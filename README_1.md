<!-- ============================================================
     KANDE MARK — GitHub Profile README
     Low-level systems engineer. Builder of worlds.
     ============================================================ -->

<div align="center">

```
██╗  ██╗ █████╗ ███╗   ██╗██████╗ ███████╗    ███╗   ███╗ █████╗ ██████╗ ██╗  ██╗
██║ ██╔╝██╔══██╗████╗  ██║██╔══██╗██╔════╝    ████╗ ████║██╔══██╗██╔══██╗██║ ██╔╝
█████╔╝ ███████║██╔██╗ ██║██║  ██║█████╗      ██╔████╔██║███████║██████╔╝█████╔╝ 
██╔═██╗ ██╔══██║██║╚██╗██║██║  ██║██╔══╝      ██║╚██╔╝██║██╔══██║██╔══██╗██╔═██╗ 
██║  ██╗██║  ██║██║ ╚████║██████╔╝███████╗    ██║ ╚═╝ ██║██║  ██║██║  ██║██║  ██╗
╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝╚═════╝ ╚══════╝    ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝
```

### `ECE student · Systems Programmer · World Builder`

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&pause=1000&color=00FF41&background=00000000&center=true&vCenter=true&width=700&lines=I+write+C+before+I+drink+coffee.;Building+systems+from+the+metal+up.;Simulating+entire+civilizations+in+SDL3.;Financial+infrastructure%2C+not+apps.;If+it+touches+hardware%2C+I'm+interested.)](https://git.io/typing-svg)

</div>

---

## `whoami`

```c
typedef struct Engineer {
    char  name[32];          /* "Kande Mark"                          */
    char  institution[64];   /* Multimedia University of Kenya, FOET  */
    char  discipline[64];    /* Electrical & Telecommunications Eng.  */
    char  location[32];      /* Meru, Kenya                           */
    int   abstraction_level; /* As low as possible                    */
    bool  stops_at_assembly; /* false — I'd go lower if I could       */
} Engineer;
```

I'm an ECE student who got tired of building TODO apps. I build **financial infrastructure**, **grand strategy simulations**, and **systems that talk directly to the machine**. My default unit of abstraction is the byte. My preferred language has manual memory management. My idea of a fun weekend is implementing a world history simulator from scratch in C with SDL3.

I don't chase frameworks. I chase **understanding**.

---

## `./projects --flagship`

### 🌍 Dominion — Grand Strategy Engine
> *A procedurally generated geopolitical world simulator. 140–160 nations. Deep simulated history, economy, language, and political systems. Built entirely in C with SDL3.*

```
Architecture:   C · SDL3 · Custom ECS · Procedural World Seed System
Inspiration:    Victoria 3 + CK3 + Hearts of Iron + Suzerain
Renderer:       Software rasterizer, cylindrical map scroll
Scope:          Nation simulation · Diplomatic AI · Economic modelling
                Language generation · Dynamic history engine
UI Aesthetic:   Victoria 3 map style × Football Manager data density
Status:         🔨 Active development
```

This isn't a game engine wrapper. This is a **simulation engine** — every nation has a procedurally generated history, cultural identity, economic structure, and political ideology derived from a single world seed. The renderer is custom. The memory model is manual. The ambition is unreasonable. That's the point.

---

### 💰 VirtualMoneySystem — Financial Infrastructure Platform
> *Open-source financial infrastructure written in C++. Not an app. Not a wallet. Infrastructure.*

```
Repository:  github.com/Kandemark/VirtualMoneySystem
Stack:       C++ · Custom transaction engine · SQLite
Design:      Self-dependent · No third-party payment rails
Vision:      CBK Regulatory Sandbox candidate
             Infrastructure layer for virtual economies
Status:      🔨 Active development
```

Built from first principles: transaction ledgers, account state machines, balance reconciliation — all implemented manually. The goal isn't to clone M-Pesa. The goal is to build the **layer beneath** M-Pesa — the kind of infrastructure a central bank would need to run a digital currency.

---

### 📦 Cargo Shipment Tracking & Delay Prediction System
> *Full-stack logistics management platform with ML-powered delay prediction. Project Lead.*

```
Stack:       Python · Django · scikit-learn · PostgreSQL
Scope:       6 Django apps · 60+ source files · REST API
ML Model:    Delay prediction pipeline trained on shipment telemetry
Deliverables: Full proposal · Pitch deck · 6-week progress reports
              Complete codebase · GitHub repository
Role:        Project Lead — sole executor of all technical deliverables
Status:      ✅ Final submission stage
```

---

### ⚡ HFT Algorithmic Trading Bot
> *High-frequency trading bot targeting prediction markets (Polymarket). Latency-obsessed.*

```
Target:      Prediction markets · Polymarket
Stack:       C · x86 Assembly (hot paths) · Custom order routing
Philosophy:  Every nanosecond is a variable. Minimize them all.
Strategy:    Market microstructure exploitation
Status:      🔬 Research & paper trading phase
```

When microseconds determine profitability, you stop using Python. You stop using C++. You start thinking about cache line alignment and branch prediction. That's where I live.

---

### 🏛️ Government e-Citizen Portal
> *Android app bringing government services to citizens. Built in Kotlin.*

```
Stack:       Kotlin · Android Studio · REST APIs
Scope:       Service access · Document management · Notifications
Status:      🔨 Active development
```

---

## `./skills --depth full`

<table>
<tr>
<td valign="top" width="33%">

### Systems & Low-Level
```
C          ████████████ Expert
C++        ██████████░░ Advanced
x86 Asm    ████████░░░░ Intermediate
SDL3       ████████░░░░ Intermediate
Make/GCC   ██████████░░ Advanced
GDB        ████████░░░░ Intermediate
```

</td>
<td valign="top" width="33%">

### Application Layer
```
Python     ██████████░░ Advanced
Django     ████████░░░░ Intermediate
Kotlin     ██████░░░░░░ Intermediate
Tkinter    ██████░░░░░░ Intermediate
```

### Data & Storage
```
SQLite     ████████░░░░ Intermediate
MySQL      ██████░░░░░░ Intermediate
PostgreSQL ██████░░░░░░ Intermediate
```

</td>
<td valign="top" width="33%">

### Tooling & Infrastructure
```
Git        ██████████░░ Advanced
VS Code    ██████████░░ Advanced
Postman    ████████░░░░ Intermediate
Claude AI  ████████████ Daily Driver
Linux      ████████░░░░ Intermediate
```

### ML / Data Science
```
scikit-learn  ██████░░░░░░
pandas        ██████░░░░░░
numpy         ██████░░░░░░
```

</td>
</tr>
</table>

---

## `./interests --verbose`

```python
interests = {
    "systems_programming":   ["memory models", "cache architecture", "SIMD", "lock-free data structures"],
    "financial_technology":  ["market microstructure", "HFT", "digital currencies", "settlement systems"],
    "game_development":      ["procedural generation", "simulation engines", "ECS architecture"],
    "geopolitical_systems":  ["nation simulation", "economic modelling", "political theory"],
    "hardware":              ["embedded systems", "signal processing", "instrumentation"],
    "currently_studying":    ["x86 internals", "compiler design", "operating system theory"],
}

philosophy = "The best abstraction is the one you wrote yourself and fully understand."
```

---

## `./currently --focus`

| Project | Phase | Stack | Priority |
|---|---|---|---|
| 🌍 **Dominion** | Nation sim engine + renderer | C · SDL3 | 🔴 High |
| 💰 **VirtualMoneySystem** | Transaction engine core | C++ | 🔴 High |
| ⚡ **HFT Bot** | Strategy research + paper trading | C · Assembly | 🟡 Medium |
| 🏛️ **e-Citizen App** | Feature development | Kotlin | 🟡 Medium |

---

## `./philosophy`

```asm
; The way I think about software:

section .text
    global _start

_start:
    ; Most engineers work here (application layer)
    ; I prefer to understand everything below this line.
    
    ; Understanding malloc() is not enough.
    ; Understanding what malloc() calls is not enough.
    ; Understanding what the kernel does is not enough.
    ; Understanding what the MMU does — now we're getting somewhere.
    
    ; Build deep. Ship real.
```

> *"I don't want to use the tool. I want to understand why the tool works — and then build a better one."*

---

## `./stats`

<div align="center">

![Kande's GitHub Stats](https://github-readme-stats.vercel.app/api?username=kandemark&show_icons=true&theme=chartreuse-dark&hide_border=true&bg_color=0d1117&title_color=00ff41&icon_color=00ff41&text_color=c9d1d9)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=kandemark&layout=compact&theme=chartreuse-dark&hide_border=true&bg_color=0d1117&title_color=00ff41&text_color=c9d1d9)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=kandemark&theme=chartreuse-dark&hide_border=true&background=0d1117&ring=00ff41&fire=00ff41&currStreakLabel=00ff41)

</div>

---

## `./contact`

```json
{
  "email":    "kandemark711@gmail.com",
  "github":   "github.com/kandemark",
  "linkedin": "linkedin.com/in/kandemark",
  "open_to":  [
    "Low-level systems collaboration",
    "Fintech infrastructure projects",
    "Game/simulation engine work",
    "Research in HFT & market systems",
    "Anything that runs closer to metal"
  ],
  "not_interested_in": [
    "CRUD app contracts",
    "Yet another REST API",
    "Anything that could be replaced by a no-code tool"
  ]
}
```

---

<div align="center">

```
╔══════════════════════════════════════════════════════════════╗
║  "Any sufficiently complex system is indistinguishable       ║
║   from magic — until you read the source code."             ║
║                                          — Kande Mark       ║
╚══════════════════════════════════════════════════════════════╝
```

*Built with obsession · Optimised with intent · Documented with pride*

![Visitor Count](https://komarev.com/ghpvc/?username=kandemark&color=00ff41&style=flat-square&label=PROFILE+VIEWS)

</div>
