# vittorionegro / writeups

```
 ██╗    ██╗██████╗ ██╗████████╗███████╗██╗   ██╗██████╗ ███████╗
 ██║    ██║██╔══██╗██║╚══██╔══╝██╔════╝██║   ██║██╔══██╗██╔════╝
 ██║ █╗ ██║██████╔╝██║   ██║   █████╗  ██║   ██║██████╔╝███████╗
 ██║███╗██║██╔══██╗██║   ██║   ██╔══╝  ██║   ██║██╔═══╝ ╚════██║
 ╚███╔███╔╝██║  ██║██║   ██║   ███████╗╚██████╔╝██║     ███████║
  ╚══╝╚══╝ ╚═╝  ╚═╝╚═╝   ╚═╝   ╚══════╝ ╚═════╝ ╚═╝     ╚══════╝
```

> documenting the process. nothing more.

---

## what this is

CTF writeups, lab walkthroughs, and exploit notes.  
Primarily HTB, with PortSwigger and TryHackMe entries as the path progresses.  
Every writeup is a post-mortem — what broke, what worked, what I'd do differently.

---

## structure

```
writeups/
├── htb/
│   ├── machines/
│   │   └── <machine-name>/
│   │       ├── README.md       ← the writeup
│   │       └── assets/         ← screenshots, scripts
│   └── challenges/
├── portswigger/
│   └── <lab-category>/
└── tryhackme/
    └── <room-name>/
```

---

## index

### hack the box — machines

| machine | os | difficulty | date | status |
|---|---|---|---|---|
| [nibbles](htb/machines/nibbles/README.md) | Linux | Easy | 2026-04-28 | ✅ |

### hack the box — challenges

| challenge | category | difficulty | status |
|---|---|---|---|
| *(coming soon)* | — | — | 🔄 |

### portswigger web academy

| lab | category | status |
|---|---|---|
| *(coming soon)* | — | 🔄 |

---

## approach

```
recon → enumeration → foothold → privesc → loot → debrief
```

no skipping steps. no guessing without a reason.  
if it took hours, the writeup reflects that.

---

## tools

nmap · gobuster · burp suite · ffuf · netcat · python  
custom scripts where it makes sense.

---

## cert path

### HTB Penetration Tester Path — 28 modules

| # | module | difficulty | est. time | status |
|---|---|---|---|---|
| 01 | Penetration Testing Process | Fundamental | 6h | 🔄 66% |
| 02 | Getting Started | Fundamental | 1d | ✅ |
| 03 | Network Enumeration with Nmap | Easy | 7h | 🔄 |
| 04 | Footprinting | Medium | 2d | 🔄 |
| 05 | Information Gathering - Web Edition | Easy | 1d | ⬜ |
| 06 | Vulnerability Assessment | Easy | 2h | ⬜ |
| 07 | File Transfers | Medium | 3h | ⬜ |
| 08 | Shells & Payloads | Medium | 2d | ⬜ |
| 09 | Using the Metasploit Framework | Easy | 5h | ⬜ |
| 10 | Password Attacks | Medium | 1d | ⬜ |
| 11 | Attacking Common Services | Medium | 1d | ⬜ |
| 12 | Pivoting, Tunneling, and Port Forwarding | Medium | 2d | ⬜ |
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

### certification sequence

```
 ✅  HTB Getting Started
 🔄  HTB Penetration Tester Path  ←  now
     ↓
 ⬜  CPTS
     ↓
 ⬜  OSCP                         ←  end goal
```

---

## site

writeups also published at **[vittorionegro.com](https://vittorionegro.com)**

---

> *writeups posted after machines retire or labs go inactive. no spoilers to live content.*
