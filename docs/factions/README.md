# Faction Management System — Overview

> LuxCity has **6 official factions** and **player-created gangs**. Each faction operates independently with its own rank structure, permissions, punishment system, and unique gameplay mechanics.

---

## Core Rules

- A player can only belong to **one faction or gang** at a time
- You can **never** issue punishments, demotions, or commands to someone of **equal or higher rank**
- **Reprimands** (the most severe punishment) can ONLY be issued by **Leader + Deputy**
- All actions are **auto-logged** to the faction audit trail
- Faction state is **saved to localStorage** and persists across sessions
- All faction finances use **$ (dollar)**

---

## Permission Tier System

Every faction follows a **universal tier system**. Ranks are grouped into tiers that determine what actions are available. The specific rank names differ per faction, but the tier powers are consistent.

| Tier | Who | Core Powers |
|------|-----|-------------|
| **Tier 7 — Leader** | Top rank (1 person) | Everything. Reprimands, disband, transfer leadership, set pay, set tax, budget signing (govt), blacklist |
| **Tier 6 — Deputy** | 2nd highest (1-2 people) | Everything except disband/transfer. Reprimands, fire/dismiss, unlimited bank, edit motto, manage recruitment |
| **Tier 5 — Senior Command** | 3rd highest (3-5 people) | Heavy punishments (laps, suspensions 24hr), promote/demote (limited range), grant bonus ($500 max), approve leave (7d), invite members |
| **Tier 4 — Junior Command** | 4th highest (5-10 people) | Medium punishments (laps, desk duty, extra shifts), promote/demote (limited), grant bonus ($300 max), approve leave (3d), invite members, create events |
| **Tier 3 — Supervisor** | 5th highest (10-15 people) | Light punishments (extra duty, verbal warnings), assign duties, approve equip requests, mentor, write reviews, moderate chat, lead squad ops |
| **Tier 2 — Senior Member** | Middle ranks | Light punishments (extra duty only), submit reports, mentor recruits, moderate chat (5 min), faction vehicles, bank withdraw (limited) |
| **Tier 1 — Regular Member** | Lower ranks | Full chat, DM, vote, request leave, bank withdraw (low limit), faction shop, faction vehicles (basic) |
| **Tier 0 — Recruit** | Entry rank | Read chat (write after 24hr), deposit only, view members, see announcements. Cannot withdraw, DM, or vote |

---

## Full Permission Matrix

```
ACTION                          T0   T1   T2   T3   T4   T5   T6   T7
──────────────────────────────  ───  ───  ───  ───  ───  ───  ───  ───
View member list                 ✓    ✓    ✓    ✓    ✓    ✓    ✓    ✓
See announcements                ✓    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Faction chat (read)              ✓    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Faction chat (write)             *    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Deposit to faction bank          ✓    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Withdraw from bank               ·    ✓    ✓    ✓    ✓    ✓    ✓    ✓
DM members                       ·    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Request leave/vacation            ·    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Vote in polls                     ·    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Use faction vehicles (basic)      ·    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Faction shop discount             ·    ✓    ✓    ✓    ✓    ✓    ✓    ✓
View online status                ·    ✓    ✓    ✓    ✓    ✓    ✓    ✓
Submit reports                    ·    ·    ✓    ✓    ✓    ✓    ✓    ✓
Mentor recruits                   ·    ·    ✓    ✓    ✓    ✓    ✓    ✓
Chat mute (5 min)                 ·    ·    ✓    ✓    ✓    ✓    ✓    ✓
Verbal warning                    ·    ·    ✓    ✓    ✓    ✓    ✓    ✓
Extra duty punishment             ·    ·    ✓    ✓    ✓    ✓    ✓    ✓
Use faction vehicles (all)        ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Assign duties                     ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Approve equip requests            ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Issue laps punishment             ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Approve leave (3 day)             ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Issue warnings (formal)           ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Write performance reviews         ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Lead squad ops                    ·    ·    ·    ✓    ✓    ✓    ✓    ✓
View activity logs                ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Chat mute (1 hr)                  ·    ·    ·    ✓    ✓    ✓    ✓    ✓
Desk/station duty punishment      ·    ·    ·    ·    ✓    ✓    ✓    ✓
Invite new members                ·    ·    ·    ·    ✓    ✓    ✓    ✓
Promote (limited range)           ·    ·    ·    ·    ✓    ✓    ✓    ✓
Demote (limited range)            ·    ·    ·    ·    ✓    ✓    ✓    ✓
Grant bonus ($300)                ·    ·    ·    ·    ✓    ·    ·    ·
Grant bonus ($500)                ·    ·    ·    ·    ·    ✓    ·    ·
Grant bonus ($5,000)              ·    ·    ·    ·    ·    ·    ✓    ·
Grant bonus (unlimited)           ·    ·    ·    ·    ·    ·    ·    ✓
Approve leave (7 day)             ·    ·    ·    ·    ✓    ✓    ✓    ✓
Officer chat access               ·    ·    ·    ·    ✓    ✓    ✓    ✓
Create faction events             ·    ·    ·    ·    ✓    ✓    ✓    ✓
View full finances                ·    ·    ·    ·    ✓    ✓    ✓    ✓
Suspend member (24hr)             ·    ·    ·    ·    ·    ✓    ✓    ✓
Approve/deny join requests        ·    ·    ·    ·    ✓    ✓    ✓    ✓
Fire/dismiss members              ·    ·    ·    ·    ·    ·    ✓    ✓
Promote (any range)               ·    ·    ·    ·    ·    ·    ✓    ✓
Edit motto/description            ·    ·    ·    ·    ·    ·    ✓    ✓
Post announcements                ·    ·    ·    ·    ·    ·    ✓    ✓
Manage recruitment mode           ·    ·    ·    ·    ·    ·    ✓    ✓
Suspend member (7 day)            ·    ·    ·    ·    ·    ·    ✓    ✓
View audit logs                   ·    ·    ·    ·    ·    ·    ✓    ✓
Set bank limits per rank          ·    ·    ·    ·    ·    ·    ✓    ✓
Unlimited bank withdraw           ·    ·    ·    ·    ·    ·    ✓    ✓
Pay dock punishment               ·    ·    ·    ·    ·    ·    ✓    ✓
REPRIMAND                         ·    ·    ·    ·    ·    ·    ✓    ✓
Set pay rates per rank            ·    ·    ·    ·    ·    ·    ·    ✓
Set faction tax %                 ·    ·    ·    ·    ·    ·    ·    ✓
Create/delete ranks               ·    ·    ·    ·    ·    ·    ·    ✓
Set rank permissions              ·    ·    ·    ·    ·    ·    ·    ✓
Transfer leadership               ·    ·    ·    ·    ·    ·    ·    ✓
Disband faction                   ·    ·    ·    ·    ·    ·    ·    ✓
Declare war/alliance              ·    ·    ·    ·    ·    ·    ·    ✓
Blacklist players                 ·    ·    ·    ·    ·    ·    ·    ✓
Edit logo/color (gangs)           ·    ·    ·    ·    ·    ·    ·    ✓
Sign budget (govt only)           ·    ·    ·    ·    ·    ·    ·    ✓

* = after 24hr probation period
```

---

## Punishment Authority by Tier

| Punishment Type | T7 | T6 | T5 | T4 | T3 | T2 |
|----------------|:--:|:--:|:--:|:--:|:--:|:--:|
| **Reprimand** (permanent record) | ✓ | ✓ | · | · | · | · |
| **Laps** (physical punishment) | ✓ | ✓ | ✓ | ✓ | ✓ | · |
| **Suspension** (24hr) | ✓ | ✓ | ✓ | · | · | · |
| **Suspension** (7 day) | ✓ | ✓ | · | · | · | · |
| **Desk/Station Duty** | ✓ | ✓ | ✓ | ✓ | · | · |
| **Extra Shifts/Overtime** | ✓ | ✓ | ✓ | ✓ | ✓ | · |
| **Verbal Warning** | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| **Chat Mute** (1hr) | ✓ | ✓ | ✓ | ✓ | ✓ | · |
| **Chat Mute** (5min) | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

---

## Rank Insignia Reference

### Police
```
RCT = ─       PO = ●       PO2 = ●●      PO3 = ●●●
CPL = ▼       DET = ◆      SGT = ▼▼▼     LT = ═
CPT = ══      CDR = ★      DC = ★★       CHIEF = ★★★
```

### Military
```
PVT = ─       PV2 = ▼      PFC = ▼●      SPC = ◆
CPL = ▼▼      SGT = ▼▼▼    SSG = ▼▼▼●    SFC = ▼▼▼●●
MSG = ▼▼▼●●●  1SG = ▼▼▼◆   SGM = ★▼▼▼    WO1 = ■
CW2 = ■■      CW3 = ■■■    2LT = ═       1LT = ══
CPT = ═══     MAJ = ★      LTC = ★★      COL = ★★★
```

### Fire
```
PFF = ─    FF = ●    ENG = ●●    LT = ═
CPT = ══   BC = ★    AC = ★★     CHIEF = ★★★
```

### Hospital
```
INT = ─    NRS = +    RES = ++    ATT = +++
CR = ═     DH = ═+    MD = ★+     CMO = ★★+
```

### Government
```
INT = ─    CLK = ●    AO = ●●    SUP = ═
DH = ══    DM = ★     CM = ★★    MAYOR = ★★★
```

### Mechanic
```
APP = ─    JR = ●     MECH = ●●    SR = ●●●
LEAD = ═   MGR = ══   CO = ★       OWNER = ★★
```

### Gang
```
ASC = ─    PSP = ▼    SLD = ▼▼    ENF = ▼▼▼
LT = ◆    UB = ◆◆    RH = ★      BOSS = ★★
```

---

## Navigation

- [Economy & Banking](economy.md)
- [Punishment System](punishment-system.md)
- [Inter-Faction Relations](inter-faction.md)
- [Shared Faction Screens](shared-screens.md)
- Per-faction: [Police](police/) · [Military](military/) · [Fire](fire/) · [Hospital](hospital/) · [Government](government/) · [Mechanic](mechanic/) · [Gangs](gangs/)
