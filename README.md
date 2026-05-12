```
 ██╗    ██╗██████╗ ██╗████████╗███████╗██╗   ██╗██████╗ ███████╗
 ██║    ██║██╔══██╗██║╚══██╔══╝██╔════╝██║   ██║██╔══██╗██╔════╝
 ██║ █╗ ██║██████╔╝██║   ██║   █████╗  ██║   ██║██████╔╝███████╗
 ██║███╗██║██╔══██╗██║   ██║   ██╔══╝  ██║   ██║██╔═══╝ ╚════██║
 ╚███╔███╔╝██║  ██║██║   ██║   ███████╗╚██████╔╝██║     ███████║
  ╚══╝╚══╝ ╚═╝  ╚═╝╚═╝   ╚═╝   ╚══════╝ ╚═════╝ ╚═╝     ╚══════╝
```

```
vittorionegro / writeups
documenting the process. nothing more.
```

---

## what this is

ctf writeups, lab walkthroughs, and exploit notes.
primarily htb, with portswigger and tryhackme as the path progresses.
every writeup is a post-mortem — what broke, what worked, what i'd do differently.

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

htb — machines

| machine | os | difficulty | date | status |
|---|---|---|---|---|
| [nibbles](htb/machines/nibbles/README.md) | linux | easy | 2026-04-28 | ✅ |

htb — challenges

| challenge | category | difficulty | status |
|---|---|---|---|
| — | — | — | ⬜ |

portswigger web academy

| lab | category | status |
|---|---|---|
| — | — | ⬜ |

---

## approach

```
recon → enumeration → foothold → privesc → loot → debrief
```

no skipping steps. no guessing without a reason.
if it took hours, the writeup reflects that.

---

## tools

```
nmap  gobuster  burp suite  ffuf  netcat  python
custom scripts where it makes sense
```

---

## htb penetration tester path · 28 modules · 6.7% complete

| # | module | difficulty | time | status |
|---|---|---|---|---|
| 01 | penetration testing process | fundamental | 6h | 🔄 |
| 02 | getting started | fundamental | 1d | ✅ |
| 03 | network enumeration with nmap | easy | 7h | 🔄 |
| 04 | footprinting | medium | 2d | 🔄 |
| 05 | information gathering - web edition | easy | 1d | ⬜ |
| 06 | vulnerability assessment | easy | 2h | ⬜ |
| 07 | file transfers | medium | 3h | ⬜ |
| 08 | shells & payloads | medium | 2d | ⬜ |
| 09 | using the metasploit framework | easy | 5h | ⬜ |
| 10 | password attacks | medium | 1d | ⬜ |
| 11 | attacking common services | medium | 1d | ⬜ |
| 12 | pivoting, tunneling, and port forwarding | medium | 2d | ⬜ |
| 13 | active directory enumeration & attacks | medium | 7d | ⬜ |
| 14 | using web proxies | easy | 1d | ⬜ |
| 15 | attacking web applications with ffuf | easy | 5h | ⬜ |
| 16 | login brute forcing | easy | 6h | ⬜ |
| 17 | sql injection fundamentals | medium | 1d | ⬜ |
| 18 | sqlmap essentials | easy | 1d | ⬜ |
| 19 | cross-site scripting (xss) | easy | 6h | ⬜ |
| 20 | file inclusion | medium | 1d | ⬜ |
| 21 | file upload attacks | medium | 1d | ⬜ |
| 22 | command injections | medium | 6h | ⬜ |
| 23 | web attacks | medium | 2d | ⬜ |
| 24 | attacking common applications | medium | 4d | ⬜ |
| 25 | linux privilege escalation | easy | 1d | ⬜ |
| 26 | windows privilege escalation | medium | 4d | ⬜ |
| 27 | documentation & reporting | easy | 2d | ⬜ |
| 28 | attacking enterprise networks | medium | 2d | ⬜ |

---

## cert path

```
✅  htb getting started
🔄  htb penetration tester path
⬜  cpts
⬜  oscp                          ← end goal
```

---

## site

[vittorionegro.com](https://vittorionegro.com)

---

writeups posted after machines retire or labs go inactive.
no spoilers to live content.
