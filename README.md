<div align="center">

# Writeups

CTF writeups and lab walkthroughs — organized by **box**, documented step by step.

<br>

![Focus](https://img.shields.io/badge/focus-offensive_security-0C447C?style=flat-square)
![Platforms](https://img.shields.io/badge/platforms-HTB_·_PortSwigger_·_THM-185FA5?style=flat-square)
![Writeups](https://img.shields.io/badge/writeups-1-9FE1CB?style=flat-square&labelColor=0F6E56)
![Maintained](https://img.shields.io/badge/maintained-yes-639922?style=flat-square)

[Machines](#-htb--machines) · [Challenges](#-htb--challenges) · [PortSwigger](#-portswigger-web-security-academy) · [CPTS progress](#-cpts-path-progress) · [Toolkit](#-toolkit)

</div>

---

## 🗂 What this is

Each writeup is reproducible: the commands I ran, why I ran them, and the dead ends worth remembering.

All work is done in authorized labs — HTB, PortSwigger, TryHackMe.

---

## 🧩 Hack The Box — Machines

<p>
  <img src="https://img.shields.io/badge/Machines_pwned-1-9FEF00?style=flat-square&logo=hackthebox&logoColor=9FEF00&labelColor=111927" />
  <img src="https://img.shields.io/badge/Challenges-0-9FEF00?style=flat-square&logo=hackthebox&logoColor=9FEF00&labelColor=111927" />
  <img src="https://img.shields.io/badge/PortSwigger_labs-0-FF6633?style=flat-square&logo=burpsuite&logoColor=FF6633&labelColor=111927" />
</p>

| Machine | OS | Difficulty | Pwned | Writeup |
|:--|:-:|:-:|:-:|:-:|
| **Nibbles** | ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) | ![Easy](https://img.shields.io/badge/Easy-2E7D32?style=flat-square) | `2026-04-28` | [![Read](https://img.shields.io/badge/Read_→-111927?style=flat-square)](machines/nibbles/README.md) |

## 🚩 Hack The Box — Challenges

—

## 🔎 PortSwigger Web Security Academy

—

---

**Certification roadmap**

```
🔄  CPTS                          ·  in progress
⬜  OSCP                          ·  end goal
```

---

## 🛠 Toolkit

The gear I reach for, grouped by attack phase.

| Phase | Tools |
|---|---|
| 🔍 **Recon** | `nmap` (+ NSE) · `gobuster` · `ffuf` · `feroxbuster` · `whatweb` · `nikto` |
| 🌐 **DNS / subdomains** | `dig` · `host` · `dnsenum` · `dnsrecon` · `fierce` · `subfinder` · `amass` |
| 🧱 **Service enum** | `smbclient` · `smbmap` · `rpcclient` · `enum4linux` · `snmpwalk` · `onesixtyone` · `showmount` |
| 🐚 **Shells** | `netcat` · `socat` · `rlwrap` |
| 🏛 **AD / Windows** | `impacket` · `crackmapexec` · `evil-winrm` |
| 🔑 **Cracking** | `hydra` · `hashcat` |
| ⚙️ **Scripting** | `python` · `bash` · `curl` · `wget` |

---

<div align="center">

[vittorionegro.com](https://vittorionegro.com)

<sub>For educational and authorized testing purposes only.</sub>

</div>
