<!-- ═══════════════════════════════════════════════════════════════════
     BINARY:   kande_mark.elf
     ARCH:     x86_64 | ARM | bare metal
     BUILD:    gcc -O3 -march=native -fno-sanitize=fun -Wall -Wobsession
     LINKER:   ld --section-start=.brain=0x00000000
     STRIPPED: no  (debug symbols kept — understanding is the point)
     ═══════════════════════════════════════════════════════════════════ -->

<div align="center">

```
┌────────────────────────────────────────────────────────────────────────┐
│  BIOS v∞.0  |  KANDEMARK SYSTEMS  |  POST SEQUENCE INITIATED          │
│  [MEM CHECK]  0x00000000 → 0xFFFFFFFFFFFFFFFF ........... OK          │
│  [CPU CHECK]  RDTSC · SSE4 · AVX2 · AMX ................. OK          │
│  [FPU CHECK]  x87 · SSE2 · precision=80bit .............. OK          │
│  [SOUL CHECK] curiosity=MAX · patience_for_noise=0 ...... OK          │
│                                                                        │
│  Loading segment descriptors...                                        │
│  Mounting /dev/brain         [████████████████████] 100%  OK          │
│  Spawning kande_mark.elf     PID=0x4B4D                               │
│  Stack base: 0x7FFFFFFF_F000   Heap: growing (no upper bound found)   │
└────────────────────────────────────────────────────────────────────────┘
```

```
██╗  ██╗ █████╗ ███╗   ██╗██████╗ ███████╗    ███╗   ███╗ █████╗ ██████╗ ██╗  ██╗
██║ ██╔╝██╔══██╗████╗  ██║██╔══██╗██╔════╝    ████╗ ████║██╔══██╗██╔══██╗██║ ██╔╝
█████╔╝ ███████║██╔██╗ ██║██║  ██║█████╗      ██╔████╔██║███████║██████╔╝█████╔╝ 
██╔═██╗ ██╔══██║██║╚██╗██║██║  ██║██╔══╝      ██║╚██╔╝██║██╔══██║██╔══██╗██╔═██╗ 
██║  ██╗██║  ██║██║ ╚████║██████╔╝███████╗    ██║ ╚═╝ ██║██║  ██║██║  ██║██║  ██╗
╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝╚═════╝ ╚══════╝    ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝
```

```asm
; Linked against: libcuriosity.so.6  libmetal.a  libobsession-static.a
; RPATH:          /usr/lib/silicon:/usr/lib/first-principles
; Entry point:    0x004B4D00  (_start → main → keep_going)
```

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&pause=1000&color=00FF41&background=00000000&center=true&vCenter=true&width=750&lines=write(STDOUT_FILENO,+coffee,+sizeof(coffee));Building+systems+from+ELF+header+to+binary+output.;Simulating+civilizations+one+tick()+at+a+time.;Financial+infrastructure+at+Ring+0.;If+it+runs+on+silicon,+I'm+already+reading+the+spec.)](https://git.io/typing-svg)

</div>

---

## `[0x0001]`  `/proc/kandemark/status`

```
Name:         kande_mark
State:        R  (running — always running)
Pid:          0x4B4D
PPid:         0x0000        ; self-bootstrapped
VmPeak:       UNDEFINED     ; still scaling
VmRSS:        EXPANDING
Threads:      1             ; focus is a finite resource
SigBlk:       0x0000000000000000
SigIgn:       0xFFFFFFFFFFFFFFFF  ; SIGFRAMEWORK — permanently masked
SigCgt:       SIGCURIOSITY        ; caught and handled — always
voluntary_ctxt_switches:    RARE  ; I don't yield lightly
nonvoluntary_ctxt_switches: 0     ; nothing preempts the build
```

```c
/* /proc/kandemark/identity — static, no dynamic dispatch */
typedef struct {
    const char  *handle;          /* "Kande Mark"                           */
    const char  *location;        /* Meru, Kenya                            */
    const char  *domain;          /* Electrical & Telecommunications Eng.   */
    uint8_t      ring_level;      /* 0x00 — Ring 0. Always.                 */
    bool         stops_at_asm;    /* false — goes lower whenever possible   */
    uintptr_t    abstraction_floor; /* (uintptr_t)0x00000001 — as low as    */
                                    /* physically legal                      */
} developer_t;

static const developer_t __attribute__((section(".identity"))) ME = {
    .handle            = "Kande Mark",
    .location          = "Meru, Kenya",
    .domain            = "ECE · Signals · Systems",
    .ring_level        = 0x00,
    .stops_at_asm      = false,
    .abstraction_floor = (uintptr_t)NULL + 1,
};
```

I build **financial infrastructure**, **geopolitical world simulations**, and **systems that speak to memory directly**.
Not wrappers. Not apps. The substrate — the layer that other software runs *on top of*.

Default unit of thought: **byte**.
Default language: manual memory management.
Default weekend project: simulate 140 nations of procedurally generated history from a single `uint64_t` seed.

---

## `[0x0002]`  `VIRTUAL ADDRESS SPACE`  `/proc/kandemark/maps`

```
╔══════════════════════════════════════════════════════════════════════════════╗
║  SEGMENT MAP — kande_mark.elf                                               ║
╠═══════════════════════════╦══════════════════════╦═════╦════════════════════╣
║  Address Range            ║  Region              ║Perm ║  Contents          ║
╠═══════════════════════════╬══════════════════════╬═════╬════════════════════╣
║  0x0000_0000–0x0FFF_FFFF  ║  .text  [ring0]      ║ r-x ║  C · x86 ASM · GDB ║
║  0x1000_0000–0x1FFF_FFFF  ║  .text  [systems]    ║ r-x ║  C++ · SDL3 · Make ║
║  0x2000_0000–0x2FFF_FFFF  ║  .data  [storage]    ║ rw- ║  SQLite · Postgres ║
║  0x3000_0000–0x3FFF_FFFF  ║  .data  [app_layer]  ║ rw- ║  Python · Django   ║
║  0x4000_0000–0x4FFF_FFFF  ║  .data  [mobile]     ║ rw- ║  Kotlin · Android  ║
║  0x5000_0000–0x5FFF_FFFF  ║  .bss   [tooling]    ║ rw- ║  Git · VSCode · GCC║
║  0x6000_0000–0x6FFF_FFFF  ║  .heap  [ml]         ║ rw- ║  sklearn · pandas  ║
║  0x7FFF_FFFF_F000         ║  [stack]             ║ rw- ║  active thought     ║
╠═══════════════════════════╬══════════════════════╬═════╬════════════════════╣
║  0xFFFF_FFFF_FFFF         ║  [vsyscall]          ║ --x ║  EAGAIN (blocked)  ║
╚═══════════════════════════╩══════════════════════╩═════╩════════════════════╝
  Note: frameworks mapped at 0xFFFF… — access denied by default
```

```
GENERAL-PURPOSE REGISTER FILE  (skill depth encoding)
┌──────────────┬──────────────────────────────────────────────┬──────────┐
│  Register    │  Value / Proficiency                         │  Latency │
├──────────────┼──────────────────────────────────────────────┼──────────┤
│  %rax  (C)   │  0xFFFF_FFFF  ████████████  EXPERT           │  0 ns    │
│  %rbx  (C++) │  0xCCCC_CCCC  ██████████░░  ADVANCED         │  1 ns    │
│  %rcx  (ASM) │  0xAAAA_AAAA  ████████░░░░  INTERMEDIATE     │  2 ns    │
│  %rdx  (SDL3)│  0xAAAA_AAAA  ████████░░░░  INTERMEDIATE     │  2 ns    │
│  %rsi  (Py)  │  0xCCCC_CCCC  ██████████░░  ADVANCED         │  6 ns    │
│  %rdi  (Git) │  0xCCCC_CCCC  ██████████░░  ADVANCED         │  1 ns    │
│  %r8 (Kotlin)│  0x8888_8888  ██████░░░░░░  PROFICIENT       │  12 ns   │
│  %r9   (GDB) │  0xAAAA_AAAA  ████████░░░░  INTERMEDIATE     │  2 ns    │
│  %r10  (SQL) │  0x8888_8888  ██████░░░░░░  PROFICIENT       │  8 ns    │
│  %r11  (ML)  │  0x8888_8888  ██████░░░░░░  PROFICIENT       │  20 ns   │
└──────────────┴──────────────────────────────────────────────┴──────────┘
  Latency = cognitive context-switch cost from primary domain (C/Systems)
```

---

## `[0x0003]`  `PROCESS TABLE`  — active work items

```
  PID      PPID    STATE     PRI    VIRT         RES        COMMAND
  ─────────────────────────────────────────────────────────────────────────
  0x0001   0x4B4D  RUNNING   -20    UNBOUNDED    GROWING    dominion.elf
  0x0002   0x4B4D  RUNNING   -20    UNBOUNDED    GROWING    virtual_money.elf
  0x0003   0x4B4D  SLEEPING   -10   BOUNDED      BOUNDED    hft_bot.elf
  0x0004   0x4B4D  BLOCKED     -5   BOUNDED      BOUNDED    ecitizen.apk
  ─────────────────────────────────────────────────────────────────────────
  SLEEPING  0x0003: voluntary — awaiting market data stream; paper trading
  BLOCKED   0x0004: I/O bound — upstream Android SDK delay
```

---

### `[0x0003:0x0001]`  `dominion.elf`  — Grand Strategy Simulation Engine

```
SECTION LAYOUT: dominion.elf
  ┌──────────────────────────────────────────────────────────────────────┐
  │  .world_seed      8 bytes  — one u64 generates an entire planet      │
  │  .nations[]       140 entries — each procedurally born from seed     │
  │  .history_engine  dynamic — time advances each tick()                │
  │  .renderer        custom software rasterizer | cylindrical scroll    │
  │  .ecs             hand-rolled entity-component system (no engine)    │
  │  .diplomacy_ai    state machine per nation | 12 behavioral modes     │
  │  .economy         supply/demand sim | trade routes | currency model  │
  │  .language_gen    phoneme engine | unique language per culture group │
  └──────────────────────────────────────────────────────────────────────┘

  CALL GRAPH (simplified):
  main()
   └─ world_init(seed)
       ├─ terrain_generate()       ; Perlin + tectonic simulation
       ├─ nation_spawn(140)        ; each nation reads from world state
       │    ├─ culture_derive()    ; from geography + neighbors
       │    ├─ language_gen()      ; phoneme-based, unique per culture
       │    └─ ideology_assign()   ; from history + resource pressure
       └─ simulation_loop()        ; tick() → update() → render()
            ├─ diplomacy_tick()
            ├─ economy_tick()
            ├─ military_tick()
            └─ sdl3_render_frame()

  BUILD:   gcc -O3 -march=native -lSDL3 -lm — no engine, no framework
  HEAP:    malloc() / free() — manual, always manual
  INSPIRE: Victoria 3 ∩ CK3 ∩ Hearts of Iron ∩ Suzerain

  STATUS:  [████████░░░░░░░░]  52% — world gen + renderer operational
```

---

### `[0x0003:0x0002]`  `virtual_money.elf`  — Financial Infrastructure Layer

```
  SYSTEM ARCHITECTURE:
  ┌──────────────────────────────────────────────────────────────────────┐
  │                                                                      │
  │   CLIENT LAYER          CORE ENGINE           PERSISTENCE           │
  │  ┌──────────┐          ┌─────────────────┐   ┌──────────────┐      │
  │  │  API     │ ────────►│ Transaction     │──►│   SQLite     │      │
  │  │  Surface │          │ Engine (C++)    │   │   Ledger     │      │
  │  └──────────┘          └────────┬────────┘   └──────────────┘      │
  │                                 │                                    │
  │              TRANSACTION STATE MACHINE                               │
  │                                                                      │
  │   PENDING ──────► VALIDATED ──────► COMMITTED ──────► SETTLED       │
  │      │                │                  │                 │        │
  │      ▼                ▼                  ▼                 ▼        │
  │   REJECTED         BOUNCED          ROLLED_BACK    RECONCILED       │
  │                                                    (terminal state) │
  └──────────────────────────────────────────────────────────────────────┘

  DESIGN AXIOMS:
    1. No third-party payment rails — self-contained or nothing
    2. Every balance mutation is a ledger entry (append-only)
    3. Settlement is idempotent — same txn_id always produces same result
    4. Auditability > convenience

  GOAL:  Not a fintech app. Not a wallet.
         The infrastructure layer that fintech apps are BUILT ON.
         If a central bank sandbox called — this would answer.

  STATUS: [████████░░░░░░░░]  49% — ledger core live, reconciler WIP
```

---

### `[0x0003:0x0003]`  `hft_bot.elf`  — High-Frequency Trading Engine

```asm
; FILE:   hft_core.asm
; TARGET: Polymarket prediction markets
; ARCH:   x86_64 — hot paths written in assembly

section .hot_path align=64      ; cache-line aligned. no negotiation.

trade_tick:
    ; Philosophy encoded in instruction selection:
    rdtsc                        ; cycle-accurate timestamp — no syscall overhead
    prefetchnta [rsi + order_q]  ; non-temporal prefetch — bypasses L3 entirely
    movdqa xmm0, [rdi]           ; aligned 128-bit SIMD load — one instruction
    ; ... strategy logic is alpha — not documented here

    ; CONSTRAINTS ENFORCED AT DESIGN TIME:
    ;   × No garbage collector                  (latency spike = loss)
    ;   × No heap allocation on hot path        (cache pollution)
    ;   × No context switches during execution  (scheduler is the enemy)
    ;   × No branch mispredictions if avoidable (pipeline stall = death)
    ;   ✓ rdtsc before and after every critical section
    ;   ✓ SIMD for order book math
    ;   ✓ Lock-free ring buffer for order queue

STRATEGY: Microstructure exploitation · Order flow imbalance detection
STATUS:   SLEEPING — paper trading active | reading market microstructure lit
```

---

### `[0x0003:0x0004]`  Cargo Shipment Delay Prediction Platform

```
  ┌──────────┐   HTTP/REST   ┌──────────────────────┐   ORM    ┌────────────┐
  │  Client  │ ────────────► │  Django (6 apps)      │ ───────► │ PostgreSQL │
  │  Browser │               │  60+ source files     │          └────────────┘
  └──────────┘               └──────────┬───────────┘
                                         │  feature pipeline
                              ┌──────────▼───────────┐
                              │  scikit-learn         │
                              │  delay prediction     │
                              │  trained on telemetry │
                              └──────────────────────┘

  ROLE:         Project Lead — sole executor of all technical deliverables
  DELIVERABLES: proposal · pitch deck · 6-week progress reports · full codebase
  STATUS:       EXITED(0) — final submission complete
```

---

### `[0x0003:0x0005]`  e-Citizen Android Government Portal

```
APK:     ecitizen.apk
STACK:   Kotlin · Android Studio · REST APIs
SCOPE:   Government service access · Document management · Push notifications
STATE:   BLOCKED — waiting on upstream I/O (Android SDK version delta)
RESUME:  On SIGCONTINUE from upstream
```

---

## `[0x0004]`  `INTERRUPT DESCRIPTOR TABLE`  — what fires a context switch

```
╔══════════╦══════════════════════════════╦══════════════════════════════════════╗
║  IRQ     ║  Vector                      ║  ISR (handler)                       ║
╠══════════╬══════════════════════════════╬══════════════════════════════════════╣
║  0x00    ║  SYSTEMS_PROGRAMMING         ║  memory_models · lock_free · SIMD    ║
║  0x01    ║  FINANCIAL_TECHNOLOGY        ║  HFT · microstructure · settlement   ║
║  0x02    ║  SIMULATION_ENGINES          ║  proc_gen · ECS · world_seeds        ║
║  0x03    ║  GEOPOLITICAL_SYSTEMS        ║  nation_sim · econ_model · politics  ║
║  0x04    ║  HARDWARE_SIGNALS            ║  embedded · DSP · instrumentation    ║
║  0x05    ║  COMPILER_INTERNALS          ║  x86_internals · IR · codegen        ║
║  0x06    ║  OPERATING_SYSTEM_THEORY     ║  scheduler · mm · syscall_dispatch   ║
╠══════════╬══════════════════════════════╬══════════════════════════════════════╣
║  0xFF    ║  SIGFRAMEWORK                ║  → /dev/null  (masked permanently)  ║
╚══════════╩══════════════════════════════╩══════════════════════════════════════╝
```

```python
# Decoded from binary — same data, higher abstraction (reluctantly)
IDT: dict = {
    0x00: ["memory models", "cache hierarchy", "SIMD", "lock-free structures"],
    0x01: ["market microstructure", "HFT", "digital currencies", "settlement"],
    0x02: ["procedural generation", "simulation engines", "ECS architecture"],
    0x03: ["nation simulation", "economic modelling", "political theory"],
    0x04: ["embedded systems", "signal processing", "instrumentation"],
    0x05: ["x86 internals", "compiler design", "IR generation", "codegen"],
    0x06: ["OS theory", "scheduler design", "memory management", "IPC"],
}

PHILOSOPHY: Final[str] = (
    "The best abstraction is the one you wrote yourself and fully understand."
)
```

---

## `[0x0005]`  `PHILOSOPHY.asm`

```asm
; FILE:     philosophy.asm
; ASSEMBLE: nasm -f elf64 philosophy.asm
; LINK:     ld -s -o philosophy philosophy.o

section .rodata
    s0   db "Most engineers stop at the API surface.",         0x0A, 0
    s1   db "Some go deeper — to the library internals.",      0x0A, 0
    s2   db "Fewer still — to the kernel.",                    0x0A, 0
    s3   db "I want to understand what the kernel calls.",     0x0A, 0
    s4   db "And what the MMU does when that call is made.",   0x0A, 0
    s5   db "Build deep. Ship real. Never stop descending.",   0x0A, 0

section .text
    global _start

_start:
    ; CALL STACK (deepest frame last — read bottom-up):
    ;
    ;  ┌─ userspace application     ← where most engineers stop
    ;  ├─ libc / stdlib             ← some look here
    ;  ├─ syscall interface         ← fewer still
    ;  ├─ kernel subsystem          ← now it gets interesting
    ;  ├─ device driver / HAL       ← this is where I live
    ;  ├─ MMU / TLB / cache         ← favorite abstraction layer
    ;  └─ silicon                   ← the actual truth
    ;
    ; Most developers build top-down and call it done.
    ; I start from the bottom and work upward.
    ; Understanding is not optional. It is the output.

    xor  rdi, rdi        ; exit code = 0  (no regrets)
    mov  rax, 60         ; SYS_exit
    syscall
```

> *"I don't want to use the tool. I want to understand why the tool works — and then build a better one."*

---

## `[0x0006]`  `STATS DUMP`

<div align="center">

![Kande's GitHub Stats](https://github-readme-stats.vercel.app/api?username=kandemark&show_icons=true&theme=chartreuse-dark&hide_border=true&bg_color=0d1117&title_color=00ff41&icon_color=00ff41&text_color=c9d1d9)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=kandemark&layout=compact&theme=chartreuse-dark&hide_border=true&bg_color=0d1117&title_color=00ff41&text_color=c9d1d9)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=kandemark&theme=chartreuse-dark&hide_border=true&background=0d1117&ring=00ff41&fire=00ff41&currStreakLabel=00ff41)

</div>

---

## `[0x0007]`  `SOCKET DESCRIPTOR TABLE`  `/proc/kandemark/fd`

```json
{
  "fd[0]": { "type": "STDIN",  "path": "/dev/curiosity",       "flags": "O_RDONLY | O_NONBLOCK" },
  "fd[1]": { "type": "STDOUT", "path": "/dev/github",          "flags": "O_WRONLY" },
  "fd[2]": { "type": "STDERR", "path": "/dev/null",            "flags": "O_WRONLY" },
  "fd[3]": { "type": "SOCK_DGRAM", "addr": "kandemark711@gmail.com" },
  "fd[4]": { "type": "SOCK_STREAM","addr": "github.com/kandemark"  },
  "fd[5]": { "type": "SOCK_STREAM","addr": "linkedin.com/in/kandemark" }
}
```

```c
/* connect() returns -1 (EAGAIN) for these request types: */
static const char *const REJECT_LIST[] = {
    "CRUD app contracts",
    "Yet another REST API wrapper",
    "Anything reproducible with a no-code tool",
    NULL,
};

/* connect() blocks until slot available — worth the wait: */
static const char *const ACCEPT_LIST[] = {
    "Low-level systems collaboration",
    "Fintech infrastructure projects",
    "Simulation / game engine work",
    "HFT and market microstructure research",
    "Anything that runs closer to silicon",
    NULL,
};
```

---

<div align="center">

```
╔══════════════════════════════════════════════════════════════════════════╗
║                                                                          ║
║   [ KERNEL PANIC — not real, just a closing statement ]                 ║
║                                                                          ║
║   "Any sufficiently complex system is indistinguishable from magic      ║
║    — until you read the source code."                                   ║
║                                                          — Kande Mark   ║
║                                                                          ║
║   RIP: 0x004B4D00  RSP: 0x7FFFFFFF_F000  RBP: 0x00000000_00000000      ║
║                                                                          ║
║   Call Trace:                                                            ║
║     [< 0x00000001 >]  curiosity_init()            ; always first        ║
║     [< 0x00000002 >]  obsession_loop()            ; runs indefinitely   ║
║     [< 0x00000003 >]  build_something_real()      ; the actual work     ║
║     [< 0x00000004 >]  understand_it_fully()       ; non-negotiable      ║
║     [< 0xFFFFFFFF >]  keep_going()                ; ← currently here    ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

```text
Compiled at -O3 · Linked with obsession · Zero undefined behavior (intentional)
```

![Visitor Count](https://komarev.com/ghpvc/?username=kandemark&color=00ff41&style=flat-square&label=LOAD_COUNT)

</div>
