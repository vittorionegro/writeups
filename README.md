<div align="center">

# 🏴 Writeups

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

> **One box = one writeup.** Full walkthrough, start to root.

Each writeup is reproducible: the commands I ran, why I ran them, and the dead ends worth remembering.

All work is done in authorized labs — HTB, PortSwigger, TryHackMe. Nothing here targets systems I don't have permission to test.

---

## 📁 The folders

| Folder | What lives here |
|---|---|
| 🧩 **`htb/machines/`** | Full HackTheBox machine walkthroughs — one folder per box, `README.md` + `assets/` |
| 🏴 **`htb/challenges/`** | HTB challenge solves — crypto, web, pwn, reversing, forensics |
| 🔎 **`portswigger/`** | PortSwigger Web Security Academy labs, grouped by category |
| 🎯 **`tryhackme/`** | TryHackMe room walkthroughs |

---

## 🧩 HTB — Machines

| Machine | OS | Difficulty | Date | Writeup |
|---|---|:---:|:---:|:---:|
| **Nibbles** | 🐧 Linux | 🟢 Easy | 2026-04-28 | [📄](htb/machines/nibbles/README.md) |

## 🏴 HTB — Challenges

| Challenge | Category | Difficulty | Writeup |
|---|---|:---:|:---:|
| *coming soon* | — | — | — |

## 🔎 PortSwigger Web Security Academy

| Lab | Category | Writeup |
|---|---|:---:|
| *coming soon* | — | — |

---

## 📊 CPTS path progress

HTB Academy Penetration Tester path: **5/28 modules done**, Vulnerability Assessment in progress.

<details>
<summary><b>📚 Full module tracker</b> (click to expand)</summary>

<br>

Legend — ✅ done · 🔄 in progress · ⬜ not started

| # | Module | Difficulty | Est. | Status |
|---|---|:---:|:---:|:---:|
| 01 | Penetration Testing Process | Fundamental | 6h | ✅ |
| 02 | Getting Started | Fundamental | 1d | ✅ |
| 03 | Network Enumeration with Nmap | Easy | 7h | ✅ |
| 04 | Footprinting | Medium | 2d | ✅ |
| 05 | Information Gathering – Web Edition | Easy | 1d | ✅ |
| 06 | Vulnerability Assessment | Easy | 2h | 🔄 |
| 07 | File Transfers | Medium | 3h | ⬜ |
| 08 | Shells & Payloads | Medium | 2d | ⬜ |
| 09 | Using the Metasploit Framework | Easy | 5h | ⬜ |
| 10 | Password Attacks | Medium | 1d | ⬜ |
| 11 | Attacking Common Services | Medium | 1d | ⬜ |
| 12 | Pivoting, Tunneling & Port Forwarding | Medium | 2d | ⬜ |
| 13 | Active Directory Enumeration & Attacks | Medium | 7d | ⬜ |
| 14 | Using Web Proxies | Easy | 1d | ⬜ |
| 15 | Attacking Web Applications with Ffuf | Easy | 5h | ⬜ |
| 16 | Login Brute Forcing | Easy | 6h | ⬜ |
| 17 | SQL Injection Fundamentals | Medium | 1d | ⬜ |
| 18 | SQLMap Essentials | Easy | 1d | ⬜ |
| 19 | Cross-Site Scripting (XSS) | Easy | 6h | ⬜ |
| 20 | File Inclusion | Medium | 1d | ⬜ |
| 21 | File Upload Attacks | Medium | 1d | ⬜ |
| 22 | Command Injections | Medium | 6h | ⬜ |
| 23 | Web Attacks | Medium | 2d | ⬜ |
| 24 | Attacking Common Applications | Medium | 4d | ⬜ |
| 25 | Linux Privilege Escalation | Easy | 1d | ⬜ |
| 26 | Windows Privilege Escalation | Medium | 4d | ⬜ |
| 27 | Documentation & Reporting | Easy | 2d | ⬜ |
| 28 | Attacking Enterprise Networks | Medium | 2d | ⬜ |

</details>

**Certification roadmap**

```
✅  HTB Penetration Tester Path   ·  in progress
🔄  CPTS                          ·  target cert
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

[vittorionegro.com](https://vittorionegro.com) · writeups mirrored on push

<sub>For educational and authorized testing purposes only. · Last updated: 2026-10-26</sub>

</div>
