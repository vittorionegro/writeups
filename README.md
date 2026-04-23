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

CTF writeups, lab walkthroughs, and exploit notes. Primarily HTB, with TryHackMe and PortSwigger entries as the path progresses. Every write-up is a post-mortem — what broke, what worked, what I'd do differently.

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

| machine | os | difficulty | status |
|---|---|---|---|
| *(in progress)* | — | — | 🔄 |

### hack the box — challenges

| challenge | category | difficulty | status |
|---|---|---|---|
| *(in progress)* | — | — | 🔄 |

### portswigger web academy

| lab | category | status |
|---|---|---|
| *(in progress)* | — | 🔄 |

---

## approach

recon → enumeration → foothold → privilege escalation → loot → debrief.

no skipping steps. no guessing without a reason. if it took hours, the writeup reflects that.

---

## tools

mostly standard. nmap, gobuster, burp, ffuf, netcat, python. custom scripts where it makes sense.

---

## cert path

```
[now]  HTB Getting Started
       ↓
       eJPT
       ↓
       OSCP  ← end goal
```

---

## site

full writeups also published at **[vittorionegro.com](https://vittorionegro.com)**

---

*writeups are posted after machines/labs are retired or no longer active. no spoilers to live content.*
