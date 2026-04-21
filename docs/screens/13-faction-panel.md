# Faction Panel — Full UI System

**Reference:** See [faction-system.md](../faction-system.md) for complete system documentation.

---

## SCREEN 13A: FACTION BROWSER (Menu → Factions)

**Element ID:** `#factionBrowser` (inside `#mmSub`)

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK              // FACTIONS                │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  ┌─────────────────────────────────────────┐   │   │
│ │  │  ☆  POLICE DEPARTMENT         387/400  │   │   │
│ │  │  ⚔   "Serve and Protect"      [JOIN]   │   │   │
│ │  └─────────────────────────────────────────┘   │   │
│ │  ┌─────────────────────────────────────────┐   │   │
│ │  │  🔥 FIRE DEPARTMENT           210/250  │   │   │
│ │  │  🪓  "First In, Last Out"      [JOIN]   │   │   │
│ │  └─────────────────────────────────────────┘   │   │
│ │  ┌─────────────────────────────────────────┐   │   │
│ │  │  ✚  HOSPITAL / EMS            350/400  │   │   │
│ │  │  ⚕   "Save Lives Daily"       [JOIN]   │   │   │
│ │  └─────────────────────────────────────────┘   │   │
│ │  ┌─────────────────────────────────────────┐   │   │
│ │  │  ★  MILITARY                  680/800  │   │   │
│ │  │  🎖   "Defend The Nation"      [JOIN]   │   │   │
│ │  └─────────────────────────────────────────┘   │   │
│ │  ┌─────────────────────────────────────────┐   │   │
│ │  │  ⚖  CITY GOVERNMENT          120/150  │   │   │
│ │  │  🏛   "For The People"         [JOIN]   │   │   │
│ │  └─────────────────────────────────────────┘   │   │
│ │  ┌─────────────────────────────────────────┐   │   │
│ │  │  ⚙  MECHANIC SHOP            190/250  │   │   │
│ │  │  🔧  "We Fix Everything"       [JOIN]   │   │   │
│ │  └─────────────────────────────────────────┘   │   │
│ │                                                │   │
│ │  ── PLAYER GANGS ──                            │   │
│ │  ┌─────────────────────────────────────────┐   │   │
│ │  │  ☠  EAST SIDE KINGS           23/50    │   │   │
│ │  │  💀  "Run These Streets"       [VIEW]   │   │   │
│ │  └─────────────────────────────────────────┘   │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13B: FACTION HOME (Dashboard — after joining)

**Element ID:** `#factionPanel`

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK                                        │   │
│ │          ┌──────────┐                          │   │
│ │          │    ☆     │                          │   │
│ │          │   ⚔️     │                          │   │
│ │          └──────────┘                          │   │
│ │      POLICE DEPARTMENT                         │   │
│ │    "Serve and Protect LuxCity"                 │   │
│ │                                                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │  YOUR RANK     ═  Lieutenant           │    │   │
│ │  │  MEMBERS       387 / 400               │    │   │
│ │  │  STATUS        ● Online                │    │   │
│ │  │  PAY RATE      $120 / cycle            │    │   │
│ │  │  TREASURY      $245,000                │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │  ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐   │   │
│ │  │ 👥 │ │ 💬 │ │ 💰 │ │ 📋 │ │ 🏖 │ │ ⚙ │   │   │
│ │  │MEMB│ │CHAT│ │BANK│ │DUTY│ │LEAV│ │SETT│   │   │
│ │  └────┘ └────┘ └────┘ └────┘ └────┘ └────┘   │   │
│ │                                                │   │
│ │           [ LEAVE FACTION ]                    │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

### Navigation Buttons

| Button | Label | Min Tier | Opens |
|--------|-------|----------|-------|
| 👥 | MEMBERS | All | Member list (paginated) |
| 💬 | CHAT | Tier 1+ | Faction chat |
| 💰 | BANK | Tier 1+ | Faction bank & transactions |
| 📋 | DUTY | Tier 3+ | Duty assignments & records |
| 🏖 | LEAVE | Tier 1+ | Leave requests (own) / approvals (Tier 3+) |
| ⚙ | SETTINGS | Tier 6+ | Faction settings (Deputy/Leader only) |

---

## SCREEN 13C: MEMBER LIST (Paginated — 10 per page)

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK        MEMBERS (387)        Page 1/39  │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ★★★ Chief Roberts            CHIEF    │    │   │
│ │  │ ⬤ Online                               │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ★★  Deputy Wong              D.CHIEF  │    │   │
│ │  │ ⬤ Online                               │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ══  Cpt. Anderson            CAPTAIN  │    │   │
│ │  │ ○ Offline                              │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ═   You                      LIEUT.   │    │   │
│ │  │ ⬤ Online                      (YOU)   │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ▼▼▼ Sgt. Martinez            SGT      │    │   │
│ │  │ ○ Offline                              │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ... (10 per page)                             │   │
│ │                                                │   │
│ │          [ ◄ PREV ]  1/39  [ NEXT ► ]         │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

**Tap on any member → opens Member Profile Popup (13D)**

---

## SCREEN 13D: MEMBER PROFILE / ACTIONS POPUP

What you see depends on YOUR rank tier vs the member's rank.

### View for Regular Members (viewing someone)

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │   Sgt. Martinez          │               │
│           │   ▼▼▼ Sergeant           │               │
│           │   ○ Offline              │               │
│           │                          │               │
│           │  JOINED   12 days ago    │               │
│           │  RECORD   2 warnings     │               │
│           │                          │               │
│           │  [💬 SEND DM]            │               │
│           │                          │               │
│           │       [ CLOSE ]          │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

### View for Supervisors (Tier 3 — Sergeant level)

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │   Ofc. Davis             │               │
│           │   ● Patrol Officer       │               │
│           │   ⬤ Online               │               │
│           │                          │               │
│           │  JOINED   30 days ago    │               │
│           │  RECORD   Clean          │               │
│           │                          │               │
│           │  ── COMMUNICATE ──       │               │
│           │  [💬 SEND DM     ]       │               │
│           │                          │               │
│           │  ── SUPERVISE ──         │               │
│           │  [📋 ASSIGN DUTY ]       │               │
│           │  [🎓 SET AS MENTOR]      │               │
│           │  [📝 WRITE REVIEW]       │               │
│           │                          │               │
│           │  ── DISCIPLINE ──        │               │
│           │  [⚠ VERBAL WARNING]      │               │
│           │  [🏃 ASSIGN LAPS ]       │               │
│           │  [⏰ EXTRA DUTY  ]       │               │
│           │  [🔇 MUTE CHAT   ]       │               │
│           │                          │               │
│           │       [ CLOSE ]          │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

### View for Officers (Tier 4-5 — Lt/Captain level)

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │   Sgt. Martinez          │               │
│           │   ▼▼▼ Sergeant           │               │
│           │   ○ Offline              │               │
│           │                          │               │
│           │  JOINED   12 days ago    │               │
│           │  RECORD   2 warnings     │               │
│           │  [📄 VIEW FULL RECORD]   │               │
│           │                          │               │
│           │  ── COMMUNICATE ──       │               │
│           │  [💬 SEND DM     ]       │               │
│           │                          │               │
│           │  ── MANAGE ──            │               │
│           │  [▲ PROMOTE      ]       │               │
│           │  [▼ DEMOTE       ]       │               │
│           │  [💰 GRANT BONUS ]       │               │
│           │  [🏖 APPROVE LEAVE]      │               │
│           │                          │               │
│           │  ── SUPERVISE ──         │               │
│           │  [📋 ASSIGN DUTY ]       │               │
│           │  [🎓 SET AS MENTOR]      │               │
│           │  [📝 WRITE REVIEW]       │               │
│           │                          │               │
│           │  ── DISCIPLINE ──        │               │
│           │  [⚠ VERBAL WARNING]      │               │
│           │  [🏃 ASSIGN LAPS ]       │               │
│           │  [🪑 DESK DUTY   ]       │               │
│           │  [⏸ SUSPEND 24HR ]       │               │
│           │  [🔇 MUTE CHAT   ]       │               │
│           │                          │               │
│           │       [ CLOSE ]          │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

### View for Deputy/Leader (Tier 6-7)

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │   Sgt. Martinez          │               │
│           │   ▼▼▼ Sergeant           │               │
│           │   ○ Offline              │               │
│           │                          │               │
│           │  JOINED   12 days ago    │               │
│           │  RECORD   2 warnings     │               │
│           │  [📄 VIEW FULL RECORD]   │               │
│           │                          │               │
│           │  ── COMMUNICATE ──       │               │
│           │  [💬 SEND DM     ]       │               │
│           │                          │               │
│           │  ── MANAGE ──            │               │
│           │  [▲ PROMOTE      ]       │               │
│           │  [▼ DEMOTE       ]       │               │
│           │  [✕ DISMISS / FIRE]      │               │
│           │  [⬆ TRANSFER LEAD]       │  ← Leader    │
│           │  [💰 GRANT BONUS ]       │               │
│           │  [🏖 APPROVE LEAVE]      │               │
│           │                          │               │
│           │  ── DISCIPLINE ──        │               │
│           │  [⚠ VERBAL WARNING]      │               │
│           │  [🏃 ASSIGN LAPS ]       │               │
│           │  [🪑 DESK DUTY   ]       │               │
│           │  [⏸ SUSPEND 7 DAY]       │               │
│           │  [💸 PAY DOCK    ]       │               │
│           │  [📛 REPRIMAND   ]       │  ← Most      │
│           │  [🔇 MUTE CHAT   ]       │    severe     │
│           │                          │               │
│           │       [ CLOSE ]          │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13E: ASSIGN LAPS MODAL

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │  🏃 ASSIGN LAPS          │               │
│           │                          │               │
│           │  TO: Ofc. Davis          │               │
│           │                          │               │
│           │  NUMBER OF LAPS          │               │
│           │  [ 1 ] [ 3 ] [ 5 ] [10] │               │
│           │                          │               │
│           │  REASON                  │               │
│           │  [Late to patrol_____]   │               │
│           │                          │               │
│           │  Route: Police Station   │               │
│           │  → Checkpoint A (100m)   │               │
│           │  → Back to Start         │               │
│           │  = ~200m per lap         │               │
│           │                          │               │
│           │  [CANCEL]    [ASSIGN]    │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13F: LAPS HUD OVERLAY (while running punishment)

```
┌──────────────────────────────────────────────────────┐
│                                                      │
│  ┌──────────────────────────────────────────┐        │
│  │  🏃 PUNISHMENT LAPS          3 / 10      │        │
│  │  → Heading to CHECKPOINT A     85m       │        │
│  │  ████████░░░░░░░░░░░░         30%        │        │
│  └──────────────────────────────────────────┘        │
│                                                      │
│                    [PLAYER]                          │
│                       │                              │
│                       │  ← route line               │
│                       ▼                              │
│                   📍 CHECKPOINT A                    │
│                                                      │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13G: FACTION CHAT

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK          💬 FACTION CHAT               │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ★★★ Chief Roberts            2m ago   │    │   │
│ │  │ All units report to HQ for briefing.   │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ═   You (YOU)                just now  │    │   │
│ │  │ Copy that, on my way.                  │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ▼▼▼ Sgt. Martinez            5m ago   │    │   │
│ │  │ Suspect spotted near the docks.        │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │ ┌──────────────────────────────┐ ┌──────┐     │   │
│ │ │ Type message...              │ │ SEND │     │   │
│ │ └──────────────────────────────┘ └──────┘     │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13H: DM CHAT (1-on-1)

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK     Sgt. Martinez     ○ Offline        │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │      ┌──────────────────────────┐              │   │
│ │      │ Need backup at the      │  ← them      │   │
│ │      │ warehouse.         5m   │              │   │
│ │      └──────────────────────────┘              │   │
│ │                                                │   │
│ │  ┌──────────────────────────┐                  │   │
│ │  │ On my way, ETA 2 min.  │  ← you           │   │
│ │  │                   just now│                  │   │
│ │  └──────────────────────────┘                  │   │
│ │                                                │   │
│ │ ┌──────────────────────────────┐ ┌──────┐     │   │
│ │ │ Type message...              │ │ SEND │     │   │
│ │ └──────────────────────────────┘ └──────┘     │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13I: FACTION BANK

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK          💰 FACTION BANK               │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  TREASURY: $245,000                            │   │
│ │  Your daily limit: $5,000 (used: $400)         │   │
│ │                                                │   │
│ │  [___Amount___]                                │   │
│ │  [ DEPOSIT ]  [ WITHDRAW ]                     │   │
│ │                                                │   │
│ │  ── RECENT TRANSACTIONS ──                     │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ▲ Chief Roberts    +$5,000    2m ago  │    │   │
│ │  │ ▼ You              -$400      1hr ago │    │   │
│ │  │ ▲ Sgt. Martinez    +$200     3hr ago  │    │   │
│ │  │ 💰 BONUS to Davis   -$300     5hr ago  │    │   │
│ │  │ 💵 SALARY payout    -$2,400   1d ago   │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13J: GRANT BONUS MODAL

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │  💰 GRANT BONUS          │               │
│           │                          │               │
│           │  TO: Sgt. Martinez       │               │
│           │                          │               │
│           │  AMOUNT                  │               │
│           │  [$____100____]          │               │
│           │  Max: $500 (your limit)  │               │
│           │                          │               │
│           │  REASON                  │               │
│           │  [Outstanding patrol__]  │               │
│           │                          │               │
│           │  Faction Bank: $245,000  │               │
│           │                          │               │
│           │  [CANCEL]    [APPROVE]   │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13K: DISCIPLINARY RECORD

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK     📄 RECORD: Sgt. Martinez           │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  STATUS: 2 warnings, 1 laps completed          │   │
│ │  REPRIMANDS: None                              │   │
│ │  RISK LEVEL: Normal                            │   │
│ │                                                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ 🏃 LAPS (5) — COMPLETED               │    │   │
│ │  │ Issued by: Lt. You                     │    │   │
│ │  │ Reason: "Abandoned patrol post"        │    │   │
│ │  │ Date: Apr 18, 2026                     │    │   │
│ │  │ Completed: Apr 18, 2026                │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ⚠ VERBAL WARNING                      │    │   │
│ │  │ Issued by: Sgt. Thompson              │    │   │
│ │  │ Reason: "Late to shift"               │    │   │
│ │  │ Date: Apr 15, 2026                    │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ⚠ VERBAL WARNING                      │    │   │
│ │  │ Issued by: Cpt. Anderson              │    │   │
│ │  │ Reason: "Improper uniform"            │    │   │
│ │  │ Date: Apr 10, 2026                    │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │          [ ◄ PREV ]  1/1  [ NEXT ► ]          │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13L: FACTION SETTINGS (Leader/Deputy)

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK          ⚙ FACTION SETTINGS            │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  MOTTO  [Serve and Protect____] [SAVE]         │   │
│ │                                                │   │
│ │  RECRUITMENT  (●)Open ( )Apply ( )Closed       │   │
│ │                                                │   │
│ │  ── PAY RATES (per cycle) ──    ← Leader only  │   │
│ │  Recruit   $10 │ Sergeant   $100               │   │
│ │  Officer   $25 │ Lieutenant $200               │   │
│ │  Officer II $50│ Captain    $500               │   │
│ │  [ EDIT PAY RATES ]                            │   │
│ │                                                │   │
│ │  ── BANK LIMITS (daily) ──     ← Leader only   │   │
│ │  Recruit $0 | Member $100 | Senior $500        │   │
│ │  Sgt $2K | Officer $10K | Deputy ∞             │   │
│ │  [ EDIT LIMITS ]                               │   │
│ │                                                │   │
│ │  ── FACTION TAX ──             ← Leader only   │   │
│ │  [ 5% ] of member earnings → treasury         │   │
│ │                                                │   │
│ │  [📋 AUDIT LOG]  [📢 ANNOUNCEMENT]            │   │
│ │                                                │   │
│ │  ── DANGER ZONE ──                             │   │
│ │  [🚫 BLACKLIST]  [⬆ TRANSFER]  [💀 DISBAND]  │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13M: AUDIT LOG (Deputy+ only)

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK          📋 AUDIT LOG                  │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ 🔺 Chief promoted Wong → D.Chief       │    │   │
│ │  │    2 hours ago                         │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ✕  Cpt. Anderson fired Recruit Mills   │    │   │
│ │  │    5 hours ago                         │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ 💰 Lt. You granted $300 bonus to Davis │    │   │
│ │  │    "Outstanding patrol" — 6 hours ago  │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ 🏃 Sgt. Martinez assigned 5 laps to    │    │   │
│ │  │    Ofc. Brown — "Late" — 1 day ago     │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ 📛 Chief issued REPRIMAND to Davis     │    │   │
│ │  │    "Repeated misconduct" — 2 days ago  │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │          [ ◄ PREV ]  1/5  [ NEXT ► ]          │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13N: GOVERNMENT BUDGET PANEL (Government faction only)

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK        💰 BUDGET ALLOCATION            │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  GOVERNMENT TREASURY: $1,000,000               │   │
│ │  TAX REVENUE THIS WEEK: $45,000                │   │
│ │                                                │   │
│ │  ── ALLOCATE FUNDS ──                          │   │
│ │  Police Dept      [$_____300,000]              │   │
│ │  Fire Dept        [$_____150,000]              │   │
│ │  Hospital/EMS     [$_____200,000]              │   │
│ │  Military         [$_____250,000]              │   │
│ │  Mechanic Shop    [$______50,000]              │   │
│ │  Gov Operations   [$______50,000]              │   │
│ │  ─────────────────────────────────             │   │
│ │  TOTAL:            $1,000,000                  │   │
│ │  REMAINING:        $0                          │   │
│ │                                                │   │
│ │  STATUS: ⏳ AWAITING MAYOR SIGNATURE           │   │
│ │                                                │   │
│ │  [PROPOSE]          ← Deputy Mayor             │   │
│ │  [APPROVE]          ← City Manager (<$100K)    │   │
│ │  [✍ SIGN & EXECUTE] ← Mayor ONLY              │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13O: MECHANIC DEPLOYMENT PANEL (Mechanic faction only)

```
┌──────────────────────────────────────────────────────┐
│ ┌────────────────────────────────────────────────┐   │
│ │ ← BACK        🔧 MECHANIC DEPLOYMENTS         │   │
│ ├────────────────────────────────────────────────┤   │
│ │                                                │   │
│ │  ── ACTIVE DEPLOYMENTS ──                      │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ●● Jake Wilson (MECHANIC)              │    │   │
│ │  │ → Police Dept  |  5 days  |  3 left    │    │   │
│ │  │ Rate: $200/day            [RECALL]     │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ●●● Carlos Ruiz (SR. MECHANIC)        │    │   │
│ │  │ → Military    |  7 days  |  6 left     │    │   │
│ │  │ Rate: $350/day            [RECALL]     │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │  ── AVAILABLE FOR DEPLOYMENT ──                │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ●● Tony Lee (MECHANIC)    ⬤ Online    │    │   │
│ │  │ [DEPLOY TO...]                         │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │  ┌────────────────────────────────────────┐    │   │
│ │  │ ═  Mike Chen (SHIFT LEAD) ○ Offline    │    │   │
│ │  │ [DEPLOY TO...]                         │    │   │
│ │  └────────────────────────────────────────┘    │   │
│ │                                                │   │
│ │  Home staff: 12 (min required: 5)              │   │
│ └────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13P: DEPLOY MECHANIC MODAL

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │  🔧 DEPLOY MECHANIC      │               │
│           │                          │               │
│           │  MEMBER: Tony Lee        │               │
│           │  RANK: ●● Mechanic       │               │
│           │                          │               │
│           │  TARGET FACTION          │               │
│           │  ( ) Police Dept         │               │
│           │  (●) Fire Dept           │               │
│           │  ( ) Hospital/EMS        │               │
│           │  ( ) Military            │               │
│           │  ( ) Government          │               │
│           │                          │               │
│           │  DURATION                │               │
│           │  [3 days] [5] [7]        │               │
│           │                          │               │
│           │  DAILY RATE              │               │
│           │  [$____200____]          │               │
│           │                          │               │
│           │  [CANCEL]    [DEPLOY]    │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

---

## SCREEN 13Q: REPRIMAND MODAL (Leader/Deputy only)

```
┌──────────────────────────────────────────────────────┐
│           ┌──────────────────────────┐               │
│           │  📛 ISSUE REPRIMAND      │               │
│           │                          │               │
│           │  ⚠ THIS IS A PERMANENT   │               │
│           │  DISCIPLINARY ACTION     │               │
│           │                          │               │
│           │  TO: Sgt. Martinez       │               │
│           │  RANK: ▼▼▼ Sergeant      │               │
│           │                          │               │
│           │  REASON                  │               │
│           │  [Repeated misconduct ]  │               │
│           │  [and failure to comply]  │               │
│           │                          │               │
│           │  EFFECTS:                │               │
│           │  • Permanent record      │               │
│           │  • Promotions blocked    │               │
│           │  • Visible to all        │               │
│           │    officers              │               │
│           │                          │               │
│           │  [CANCEL]    [CONFIRM]   │               │
│           └──────────────────────────┘               │
└──────────────────────────────────────────────────────┘
```

---

## TOTAL SCREENS IN FACTION SYSTEM: 17

| ID | Screen | Type |
|----|--------|------|
| 13A | Faction Browser | Redesigned |
| 13B | Faction Home (Dashboard) | New |
| 13C | Member List (Paginated) | New |
| 13D | Member Profile/Actions Popup | New (4 variants by tier) |
| 13E | Assign Laps Modal | New |
| 13F | Laps HUD Overlay | New |
| 13G | Faction Chat | New |
| 13H | DM Chat (1-on-1) | New |
| 13I | Faction Bank | New |
| 13J | Grant Bonus Modal | New |
| 13K | Disciplinary Record | New |
| 13L | Faction Settings | Redesigned |
| 13M | Audit Log | New |
| 13N | Government Budget Panel | New (Govt only) |
| 13O | Mechanic Deployment Panel | New (Mechanic only) |
| 13P | Deploy Mechanic Modal | New (Mechanic only) |
| 13Q | Reprimand Modal | New |
