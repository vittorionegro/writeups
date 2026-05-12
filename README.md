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
