# LUXCITY FACTION MANAGEMENT SYSTEM

> Complete documentation of the faction system, rank permissions, punishment mechanics, inter-faction relationships, government budget control, and cross-faction assignments.

---

## TABLE OF CONTENTS

1. [System Overview](#1-system-overview)
2. [Permission Tier System](#2-permission-tier-system)
3. [Police Department](#3-police-department)
4. [Military](#4-military)
5. [Fire Department](#5-fire-department)
6. [Hospital / EMS](#6-hospital--ems)
7. [City Government](#7-city-government)
8. [Mechanic Shop](#8-mechanic-shop)
9. [Player Gangs](#9-player-gangs)
10. [Punishment System](#10-punishment-system)
11. [Laps Punishment Mechanic](#11-laps-punishment-mechanic)
12. [Disciplinary Records](#12-disciplinary-records)
13. [Government Budget Control System](#13-government-budget-control-system)
14. [Mechanic Cross-Faction Assignment System](#14-mechanic-cross-faction-assignment-system)
15. [Inter-Faction Relationships](#15-inter-faction-relationships)
16. [Faction Bank & Economy](#16-faction-bank--economy)

---

## 1. SYSTEM OVERVIEW

LuxCity has **6 official factions** and **player-created gangs**. Each faction operates independently with its own rank structure, permissions, punishment system, and unique gameplay mechanics. Factions are interconnected through the **Government Budget System** (government distributes funds) and the **Mechanic Assignment System** (mechanics deployed to other factions).

### Currency
All faction finances use **$ (dollar)**.

### Core Rules
- A player can only belong to **one faction or gang** at a time
- You can **never** issue punishments, demotions, or commands to someone of **equal or higher rank**
- **Reprimands** (the most severe punishment) can ONLY be issued by **Leader + Deputy**
- All actions are **auto-logged** to the faction audit trail
- Faction state is **saved to localStorage** and persists across sessions

---

## 2. PERMISSION TIER SYSTEM

Every faction follows a **universal tier system**. Regardless of the faction, ranks are grouped into tiers that determine what actions are available. The specific rank names differ per faction, but the tier powers are consistent.

### Tier Overview

| Tier | Who | Core Powers |
|------|-----|-------------|
| **TIER 7 — Leader** | Top rank (1 person) | Everything. Reprimands, disband, transfer leadership, set pay, set tax, budget signing (govt), blacklist |
| **TIER 6 — Deputy** | 2nd highest (1-2 people) | Everything except disband/transfer. Reprimands, fire/dismiss, unlimited bank, edit motto, manage recruitment |
| **TIER 5 — Senior Command** | 3rd highest (3-5 people) | Heavy punishments (laps, suspensions 24hr), promote/demote (limited range), grant bonus ($500 max), approve leave (7d), invite members |
| **TIER 4 — Junior Command** | 4th highest (5-10 people) | Medium punishments (laps, desk duty, extra shifts), promote/demote (limited), grant bonus ($300 max), approve leave (3d), invite members, create events |
| **TIER 3 — Supervisor** | 5th highest (10-15 people) | Light punishments (extra duty, verbal warnings), assign duties, approve equip requests, mentor, write reviews, moderate chat, lead squad ops |
| **TIER 2 — Senior Member** | Middle ranks | Light punishments (extra duty only), submit reports, mentor recruits, moderate chat (5 min), faction vehicles, bank withdraw (limited) |
| **TIER 1 — Regular Member** | Lower ranks | Full chat, DM, vote, request leave, bank withdraw (low limit), faction shop, faction vehicles (basic) |
| **TIER 0 — Recruit** | Entry rank | Read chat (write after 24hr), deposit only, view members, see announcements. Cannot withdraw, DM, or vote |

### Punishment Authority by Tier

| Punishment Type | Tier 7 (Leader) | Tier 6 (Deputy) | Tier 5 (Sr. Cmd) | Tier 4 (Jr. Cmd) | Tier 3 (Supervisor) | Tier 2 (Sr. Member) |
|----------------|:---:|:---:|:---:|:---:|:---:|:---:|
| **Reprimand** (permanent record) | YES | YES | - | - | - | - |
| **Laps** (physical punishment) | YES | YES | YES | YES | YES | - |
| **Suspension** (24hr access restrict) | YES | YES | YES | - | - | - |
| **Suspension** (7 day) | YES | YES | - | - | - | - |
| **Desk/Station Duty** | YES | YES | YES | YES | - | - |
| **Extra Shifts/Overtime** | YES | YES | YES | YES | YES | - |
| **Verbal Warning** | YES | YES | YES | YES | YES | YES |
| **Chat Mute** (1hr) | YES | YES | YES | YES | YES | - |
| **Chat Mute** (5min) | YES | YES | YES | YES | YES | YES |

**Rule: You can ONLY punish ranks BELOW yours. Never equal or above.**

---

## 3. POLICE DEPARTMENT

**Color:** #4488ff (Blue)
**Logo:** Shield with star (☆⚔)
**Motto:** "Serve and Protect LuxCity"
**Max Members:** 400

### Rank Structure

| Index | Rank | Abbr | Insignia | Tier | Max Slots |
|-------|------|------|----------|------|-----------|
| 0 | Academy Recruit | RCT | ─ | Tier 0 (Recruit) | 85 |
| 1 | Patrol Officer | PO | ● | Tier 1 (Regular) | 72 |
| 2 | Police Officer II | PO2 | ●● | Tier 1 (Regular) | 60 |
| 3 | Police Officer III | PO3 | ●●● | Tier 1 (Regular) | 50 |
| 4 | Corporal | CPL | ▼ | Tier 2 (Senior) | 40 |
| 5 | Detective | DET | ◆ | Tier 2 (Senior) | 35 |
| 6 | Sergeant | SGT | ▼▼▼ | Tier 3 (Supervisor) | 25 |
| 7 | Lieutenant | LT | ═ | Tier 4 (Jr. Command) | 15 |
| 8 | Captain | CPT | ══ | Tier 5 (Sr. Command) | 10 |
| 9 | Commander | CDR | ★ | Tier 5 (Sr. Command) | 5 |
| 10 | Deputy Chief | DC | ★★ | Tier 6 (Deputy) | 2 |
| 11 | Chief of Police | CHIEF | ★★★ | Tier 7 (Leader) | 1 |

### Unique Police Actions

| Action | Min Rank | Description |
|--------|----------|-------------|
| Issue APB (All Points Bulletin) | Sergeant (6) | Alert all faction members about a suspect/situation |
| File Arrest Report | Patrol Officer (1) | Log an arrest for faction records |
| Set Patrol Zone | Lieutenant (7) | Assign patrol areas on the map for officers |
| Issue Citation | Corporal (4) | Issue a ticket/citation to a civilian |
| Authorize Pursuit | Captain (8) | Approve high-speed vehicle pursuits |
| Call SWAT | Commander (9) | Escalate a situation to maximum response |
| Internal Affairs Review | Deputy Chief (10) | Investigate officer misconduct |
| Change Department Policy | Chief (11) | Modify department-wide rules and procedures |

### Police-Specific Punishments

| Punishment | Min Rank to Issue | Effect |
|-----------|-------------------|--------|
| Desk Duty | Lieutenant (7) | Restricted from patrol, must stay at station |
| Badge Suspension | Captain (8) | Temporarily lose rank privileges for 24hrs |
| Laps around Precinct | Sergeant (6) | Must complete running laps with checkpoints |
| Report Writing | Corporal (4) | Assigned extra paperwork (busy work) |
| Reprimand | Deputy Chief (10) | Permanent mark on record, affects promotion eligibility |
| Internal Investigation | Deputy Chief (10) | Full review of officer conduct |

---

## 4. MILITARY

**Color:** #6a8a4a (Army Green)
**Logo:** Star with eagle (★🎖)
**Motto:** "Defend LuxCity and Maintain Security"
**Max Members:** 800

### Rank Structure

| Index | Rank | Abbr | Insignia | Tier | Max Slots |
|-------|------|------|----------|------|-----------|
| 0 | Private | PVT | ─ | Tier 0 (Recruit) | 167 |
| 1 | Private 2nd Class | PV2 | ▼ | Tier 0 (Recruit) | 140 |
| 2 | Private First Class | PFC | ▼● | Tier 1 (Regular) | 110 |
| 3 | Specialist | SPC | ◆ | Tier 1 (Regular) | 80 |
| 4 | Corporal | CPL | ▼▼ | Tier 1 (Regular) | 65 |
| 5 | Sergeant | SGT | ▼▼▼ | Tier 2 (Senior) | 55 |
| 6 | Staff Sergeant | SSG | ▼▼▼● | Tier 2 (Senior) | 40 |
| 7 | Sergeant First Class | SFC | ▼▼▼●● | Tier 2 (Senior) | 25 |
| 8 | Master Sergeant | MSG | ▼▼▼●●● | Tier 3 (Supervisor) | 15 |
| 9 | First Sergeant | 1SG | ▼▼▼◆ | Tier 3 (Supervisor) | 10 |
| 10 | Sergeant Major | SGM | ★▼▼▼ | Tier 3 (Supervisor) | 5 |
| 11 | Warrant Officer 1 | WO1 | ■ | Tier 3 (Supervisor) | 15 |
| 12 | Chief WO 2 | CW2 | ■■ | Tier 3 (Supervisor) | 12 |
| 13 | Chief WO 3 | CW3 | ■■■ | Tier 4 (Jr. Command) | 8 |
| 14 | Second Lieutenant | 2LT | ═ | Tier 4 (Jr. Command) | 20 |
| 15 | First Lieutenant | 1LT | ══ | Tier 4 (Jr. Command) | 15 |
| 16 | Captain | CPT | ═══ | Tier 5 (Sr. Command) | 10 |
| 17 | Major | MAJ | ★ | Tier 5 (Sr. Command) | 5 |
| 18 | Lieutenant Colonel | LTC | ★★ | Tier 6 (Deputy) | 2 |
| 19 | Colonel | COL | ★★★ | Tier 7 (Leader) | 1 |

### Unique Military Actions

| Action | Min Rank | Description |
|--------|----------|-------------|
| Issue Orders | Master Sergeant (8) | Formal orders down the chain of command |
| Deploy Squad | First Lieutenant (15) | Send a squad to a specific map zone |
| Requisition Weapons | Captain (16) | Request weapons/vehicles from armory |
| Authorize Strike | Major (17) | Approve offensive operations |
| Court Martial Proceedings | Lt. Colonel (18) | Formal military trial for serious offenses |
| Declare Base Lockdown | Colonel (19) | Lock down military base, restrict access |
| Change ROE (Rules of Engagement) | Colonel (19) | Modify engagement rules for all troops |

### Military-Specific Punishments

| Punishment | Min Rank to Issue | Effect |
|-----------|-------------------|--------|
| Laps / PT Punishment | Master Sergeant (8) | Running laps with full checkpoint system |
| Push-Up Detail | Sergeant (5) | Extra physical training assignment |
| KP Duty (Kitchen Patrol) | Staff Sergeant (6) | Assigned to kitchen/mess hall duty |
| Guard Duty (Extra Shifts) | Master Sergeant (8) | Extended guard post assignments |
| Barracks Restriction | First Lieutenant (15) | Confined to base for set duration |
| Article 15 (Non-judicial) | Captain (16) | Formal disciplinary action, loss of pay |
| Court Martial | Lt. Colonel (18) | Severe — can result in demotion or discharge |
| Reprimand | Lt. Colonel (18) | Permanent record, blocks promotions |

---

## 5. FIRE DEPARTMENT

**Color:** #ff6622 (Orange-Red)
**Logo:** Fire axe with flame (🔥🪓)
**Motto:** "First In, Last Out"
**Max Members:** 250

### Rank Structure

| Index | Rank | Abbr | Insignia | Tier | Max Slots |
|-------|------|------|----------|------|-----------|
| 0 | Probationary FF | PFF | ─ | Tier 0 (Recruit) | 100 |
| 1 | Firefighter | FF | ● | Tier 1 (Regular) | 77 |
| 2 | Driver/Engineer | ENG | ●● | Tier 2 (Senior) | 35 |
| 3 | Lieutenant | LT | ═ | Tier 3 (Supervisor) | 20 |
| 4 | Captain | CPT | ══ | Tier 4 (Jr. Command) | 10 |
| 5 | Battalion Chief | BC | ★ | Tier 5 (Sr. Command) | 5 |
| 6 | Assistant Chief | AC | ★★ | Tier 6 (Deputy) | 2 |
| 7 | Fire Chief | CHIEF | ★★★ | Tier 7 (Leader) | 1 |

### Unique Fire Actions

| Action | Min Rank | Description |
|--------|----------|-------------|
| Dispatch Fire Call | Lieutenant (3) | Send units to a fire/emergency location |
| Assign Station Duties | Lieutenant (3) | Assign members to specific fire stations |
| Schedule Drills | Captain (4) | Set up training drill sessions |
| Equipment Inspection | Driver/Engineer (2) | Log equipment checks on trucks/gear |
| Approve Overtime | Battalion Chief (5) | Authorize extra shift pay |
| Change Response Protocol | Assistant Chief (6) | Modify emergency response procedures |
| Station Reallocation | Fire Chief (7) | Reassign personnel across all stations |

### Fire-Specific Punishments

| Punishment | Min Rank to Issue | Effect |
|-----------|-------------------|--------|
| Station Cleanup | Lieutenant (3) | Full cleaning of assigned fire station |
| Equipment Maintenance | Lieutenant (3) | Extra equipment servicing duty |
| Laps around Station | Lieutenant (3) | Running laps with checkpoints |
| Extra Drill Sessions | Captain (4) | Additional training drills |
| Tower Climb Punishment | Captain (4) | Repeated tower/stair climbs |
| Probation Extension | Battalion Chief (5) | Extend probationary period |
| Reprimand | Assistant Chief (6) | Permanent record mark |

---

## 6. HOSPITAL / EMS

**Color:** #22cc66 (Green)
**Logo:** Medical cross with caduceus (✚⚕)
**Motto:** "Save Lives, Heal the Wounded"
**Max Members:** 400

### Rank Structure

| Index | Rank | Abbr | Insignia | Tier | Max Slots |
|-------|------|------|----------|------|-----------|
| 0 | Intern | INT | ─ | Tier 0 (Recruit) | 154 |
| 1 | Nurse | NRS | + | Tier 1 (Regular) | 120 |
| 2 | Resident | RES | ++ | Tier 1 (Regular) | 60 |
| 3 | Attending Physician | ATT | +++ | Tier 2 (Senior) | 40 |
| 4 | Chief Resident | CR | ═ | Tier 3 (Supervisor) | 15 |
| 5 | Department Head | DH | ═+ | Tier 4 (Jr. Command) | 8 |
| 6 | Medical Director | MD | ★+ | Tier 6 (Deputy) | 2 |
| 7 | Chief Medical Officer | CMO | ★★+ | Tier 7 (Leader) | 1 |

### Unique Hospital Actions

| Action | Min Rank | Description |
|--------|----------|-------------|
| Assign ER Shifts | Chief Resident (4) | Schedule members for emergency room duty |
| Patient Log Entry | Nurse (1) | Log patient treatment records |
| Medical Supply Request | Resident (2) | Request supplies from inventory |
| On-Call Rotation | Department Head (5) | Set who is on-call for emergencies |
| Approve Procedures | Department Head (5) | Authorize complex medical operations |
| Change Treatment Protocol | Medical Director (6) | Modify standard treatment procedures |
| Budget Medical Supplies | CMO (7) | Allocate budget for medical equipment |

### Hospital-Specific Punishments

| Punishment | Min Rank to Issue | Effect |
|-----------|-------------------|--------|
| Double Shifts | Chief Resident (4) | Assigned consecutive shifts |
| Record Filing Duty | Attending Physician (3) | Must organize patient records |
| Supply Room Inventory | Chief Resident (4) | Full inventory count of supply room |
| Laps around Hospital | Chief Resident (4) | Running laps with checkpoints |
| Bedpan Duty | Department Head (5) | Assigned to menial cleanup tasks |
| License Review | Medical Director (6) | Formal review that blocks promotions |
| Reprimand | Medical Director (6) | Permanent record mark |

---

## 7. CITY GOVERNMENT

**Color:** #ffd700 (Gold)
**Logo:** Scales of justice with building (⚖🏛)
**Motto:** "For the People of LuxCity"
**Max Members:** 150

### Rank Structure

| Index | Rank | Abbr | Insignia | Tier | Max Slots |
|-------|------|------|----------|------|-----------|
| 0 | Intern | INT | ─ | Tier 0 (Recruit) | 55 |
| 1 | Clerk | CLK | ● | Tier 1 (Regular) | 40 |
| 2 | Admin Officer | AO | ●● | Tier 2 (Senior) | 25 |
| 3 | Dept Supervisor | SUP | ═ | Tier 3 (Supervisor) | 15 |
| 4 | Department Head | DH | ══ | Tier 4 (Jr. Command) | 8 |
| 5 | Deputy Mayor | DM | ★ | Tier 5 (Sr. Command) | 4 |
| 6 | City Manager | CM | ★★ | Tier 6 (Deputy) | 2 |
| 7 | Mayor | MAYOR | ★★★ | Tier 7 (Leader) | 1 |

### Unique Government Actions — BUDGET CONTROL

The Government is **the most powerful faction economically**. It controls how money flows to ALL other factions. See [Section 13: Government Budget Control System](#13-government-budget-control-system) for full details.

| Action | Min Rank | Description |
|--------|----------|-------------|
| Draft City Policy | Dept Supervisor (3) | Propose new city rules (needs approval) |
| Review Budget Proposal | Department Head (4) | Review and comment on budget allocations |
| Issue City Permits | Department Head (4) | Grant permits for events/construction |
| Propose Budget Allocation | Deputy Mayor (5) | Draft how funds are distributed to factions |
| Approve Minor Spending | Deputy Mayor (5) | Approve expenditures under $10,000 |
| Schedule Council Meeting | City Manager (6) | Set agenda for faction budget meetings |
| Approve Budget Allocation | City Manager (6) | Can approve budgets up to $100,000 |
| **Sign Budget (Final Authority)** | **Mayor (7)** | **ONLY the Mayor can sign and execute faction budget distributions** |
| Declare City Emergency | Mayor (7) | Unlock emergency funds for all factions |
| Set Faction Tax Rate | Mayor (7) | Set the % tax each faction pays to government |

### Government-Specific Punishments

| Punishment | Min Rank to Issue | Effect |
|-----------|-------------------|--------|
| Overtime Paperwork | Dept Supervisor (3) | Extra administrative filing |
| Public Service Duty | Department Head (4) | Assigned to community cleanup |
| Laps around City Hall | Dept Supervisor (3) | Running laps with checkpoints |
| Office Restriction | Deputy Mayor (5) | Confined to desk, no field work |
| Pay Dock | City Manager (6) | Temporary reduction in salary |
| Formal Censure | City Manager (6) | Public reprimand, visible to all |
| Reprimand | City Manager (6) | Permanent record mark |

---

## 8. MECHANIC SHOP

**Color:** #ffaa22 (Orange)
**Logo:** Gear with wrench (⚙🔧)
**Motto:** "We Fix Everything"
**Max Members:** 250

### Rank Structure

| Index | Rank | Abbr | Insignia | Tier | Max Slots |
|-------|------|------|----------|------|-----------|
| 0 | Apprentice | APP | ─ | Tier 0 (Recruit) | 90 |
| 1 | Junior Mechanic | JR | ● | Tier 1 (Regular) | 72 |
| 2 | Mechanic | MECH | ●● | Tier 2 (Senior) | 45 |
| 3 | Senior Mechanic | SR | ●●● | Tier 3 (Supervisor) | 25 |
| 4 | Shift Lead | LEAD | ═ | Tier 4 (Jr. Command) | 10 |
| 5 | Service Manager | MGR | ══ | Tier 5 (Sr. Command) | 5 |
| 6 | Co-Owner | CO | ★ | Tier 6 (Deputy) | 2 |
| 7 | Shop Owner | OWNER | ★★ | Tier 7 (Leader) | 1 |

### Unique Mechanic Actions — CROSS-FACTION DEPLOYMENT

The Mechanic Shop has a **unique system** where members can be **assigned to other factions** as their dedicated mechanic. See [Section 14: Mechanic Cross-Faction Assignment System](#14-mechanic-cross-faction-assignment-system) for full details.

| Action | Min Rank | Description |
|--------|----------|-------------|
| Accept Repair Job | Junior Mechanic (1) | Take a vehicle repair job from the queue |
| Manage Parts Inventory | Mechanic (2) | Track and order replacement parts |
| Set Service Prices | Shift Lead (4) | Set repair/customization pricing |
| Assign Repair Jobs | Senior Mechanic (3) | Assign specific jobs to mechanics |
| **Deploy Mechanic to Faction** | **Service Manager (5)** | Assign a mechanic to serve another faction |
| **Recall Mechanic** | **Service Manager (5)** | Pull a mechanic back from faction deployment |
| Customer Priority Queue | Shift Lead (4) | Set which repair jobs take priority |
| Approve Custom Builds | Service Manager (5) | Authorize expensive vehicle modifications |
| Set Deployment Duration | Co-Owner (6) | Set how long a mechanic serves another faction |
| Negotiate Contracts | Co-Owner (6) | Set payment terms with other factions |
| Manage All Deployments | Shop Owner (7) | Full control over all cross-faction assignments |

### Who Can Be Deployed?

**Only ranks 2-4 (Mechanic, Senior Mechanic, Shift Lead) can be assigned to other factions.** Apprentices and Junior Mechanics are too inexperienced. Service Manager and above are needed to run the shop.

### Mechanic-Specific Punishments

| Punishment | Min Rank to Issue | Effect |
|-----------|-------------------|--------|
| Shop Cleanup | Senior Mechanic (3) | Full cleaning of the workshop |
| Inventory Count | Senior Mechanic (3) | Manual count of all parts/tools |
| Laps around Shop | Senior Mechanic (3) | Running laps with checkpoints |
| Extra Repair Quota | Shift Lead (4) | Must complete extra repair jobs |
| Oil Change Only | Service Manager (5) | Restricted to basic jobs only (no custom work) |
| Tool Confiscation | Service Manager (5) | Temporarily lose access to advanced tools |
| Reprimand | Co-Owner (6) | Permanent record mark |

---

## 9. PLAYER GANGS

**Color:** Player-selected from palette
**Logo:** Skull (☠💀)
**Max Members:** 50
**Created by:** Players at Gang HQ (costs $1,000)

### Rank Structure

| Index | Rank | Abbr | Insignia | Tier | Max Slots |
|-------|------|------|----------|------|-----------|
| 0 | Associate | ASC | ─ | Tier 0 (Recruit) | 12 |
| 1 | Prospect | PSP | ▼ | Tier 1 (Regular) | 10 |
| 2 | Soldier | SLD | ▼▼ | Tier 2 (Senior) | 10 |
| 3 | Enforcer | ENF | ▼▼▼ | Tier 3 (Supervisor) | 7 |
| 4 | Lieutenant | LT | ◆ | Tier 4 (Jr. Command) | 5 |
| 5 | Underboss | UB | ◆◆ | Tier 5 (Sr. Command) | 3 |
| 6 | Right Hand | RH | ★ | Tier 6 (Deputy) | 2 |
| 7 | Boss / OG | BOSS | ★★ | Tier 7 (Leader) | 1 |

### Unique Gang Actions

| Action | Min Rank | Description |
|--------|----------|-------------|
| Assign Turf | Enforcer (3) | Mark territory zones on the map |
| Plan Heist | Lieutenant (4) | Set up crew for a heist mission |
| Collect Tribute | Enforcer (3) | Collect $ from gang activities |
| Set Tribute Rate | Underboss (5) | Set % tax on gang member earnings |
| Drug/Weapon Distribution | Lieutenant (4) | Assign distribution routes |
| Declare Gang War | Right Hand (6) | Start conflict with another gang |
| Negotiate Alliance | Right Hand (6) | Propose alliance with another gang |
| Set Gang Color/Logo | Boss (7) | Change gang appearance |

### Gang-Specific Punishments

| Punishment | Min Rank to Issue | Effect |
|-----------|-------------------|--------|
| Laps around Turf | Enforcer (3) | Running laps through gang territory |
| Beat Down | Enforcer (3) | Take damage as punishment (lose HP) |
| Tribute Penalty | Lieutenant (4) | Must pay extra tribute for a period |
| Turf Watch (Extra Guard) | Enforcer (3) | Extended guard duty on territory |
| Exile Threat | Underboss (5) | Final warning before dismissal |
| Reprimand | Right Hand (6) | Permanent record, blocks rank up |

---

## 10. PUNISHMENT SYSTEM

### Overview

The punishment system is a core part of faction discipline. It creates real gameplay consequences — when a member is punished, they must **physically complete the punishment** in the game world.

### Punishment Types

#### 1. VERBAL WARNING (Tier 2+)
- Lightest punishment
- Logged in member's record
- No gameplay effect
- 3 verbal warnings = auto-escalation to supervisor

#### 2. CHAT MUTE
- **5 minutes:** Tier 2+ can issue
- **1 hour:** Tier 3+ can issue
- Member cannot send messages in faction chat during mute

#### 3. EXTRA DUTY / SHIFTS (Tier 3+)
- Assigned additional tasks (patrol, guard, cleanup, etc.)
- Shows as active assignment on member's profile
- Must be completed to clear

#### 4. LAPS (Tier 3+) — See Section 11
- Physical running punishment with checkpoint system
- Most common punishment across all factions
- 1-10 laps can be assigned
- Each lap has a defined route with checkpoints

#### 5. DESK/STATION DUTY (Tier 4+)
- Restricted from field activities
- Must remain at faction HQ
- Duration: 1-24 hours (game time)

#### 6. SUSPENSION (Tier 5+ for 24hr, Tier 6+ for 7 day)
- Temporarily lose rank privileges
- Cannot access faction bank
- Cannot participate in faction activities
- Still visible in member list as "SUSPENDED"

#### 7. PAY DOCK (Tier 6+ only)
- Salary reduced by 50% for a set period
- Duration: 1-7 cycles

#### 8. REPRIMAND (Tier 7 Leader + Tier 6 Deputy ONLY)
- **The most severe punishment short of dismissal**
- Creates a **permanent mark** on member's disciplinary record
- Blocks promotions until the reprimand is reviewed and lifted
- Visible to all officers when viewing the member's profile
- Can only be lifted by Leader or Deputy
- Logged with: date, reason, who issued it, and current status (active/lifted)

---

## 11. LAPS PUNISHMENT MECHANIC

### How It Works

1. **Issuing:** An authorized officer opens a member's profile, taps "Assign Laps", selects number of laps (1-10), and enters a reason
2. **Notification:** The punished member receives a notification: "You have been assigned X laps by [Officer Name]. Reason: [reason]"
3. **Checkpoint Route:** The game generates a **lap route** near the faction HQ with visible checkpoint markers:
   - **START/FINISH** marker (green flag)
   - **CHECKPOINT A** (halfway point, blue marker)
   - The member must run from START → CHECKPOINT A → back to START = 1 lap
   - Route is approximately 200m per lap
4. **Tracking:** A HUD overlay shows:
   - Current lap: 3/10
   - Checkpoint: heading to A / heading back
   - Distance to next checkpoint
5. **Completion:** When all laps are done, a notification is sent to the issuing officer and logged
6. **Consequences of not completing:** Laps remain active until completed. After 24hr without completion, auto-escalated to next punishment tier

### Checkpoint Locations (Per Faction)

| Faction | Start Point | Checkpoint A |
|---------|------------|--------------|
| Police | Police Station front | 100m down the street |
| Military | Base gate | Perimeter fence corner |
| Fire | Fire Station bay | Around the block |
| Hospital | Hospital entrance | Parking lot perimeter |
| Government | City Hall steps | Around the plaza |
| Mechanic | Shop front | Down the road and back |
| Gang | Gang HQ | Through turf territory |

---

## 12. DISCIPLINARY RECORDS

Every faction member has a **disciplinary record** that is automatically maintained.

### Record Entry Format

Each entry contains:
- **Date/Time:** When the action was taken
- **Type:** Warning / Laps / Suspension / Desk Duty / Reprimand / etc.
- **Issued By:** Name and rank of the officer who issued it
- **Reason:** Text description of why
- **Status:** Active / Completed / Lifted (for reprimands)
- **Duration:** If applicable (suspension length, number of laps)

### Record Visibility

| Viewer's Tier | What They Can See |
|---------------|-------------------|
| Tier 0-1 (Recruit/Regular) | Own record only |
| Tier 2 (Senior) | Own record only |
| Tier 3 (Supervisor) | Records of members they supervise (below their rank) |
| Tier 4-5 (Command) | All records of ranks below them |
| Tier 6-7 (Deputy/Leader) | ALL records, can edit/lift reprimands |

### Record Consequences

- **3 Verbal Warnings** within 7 days → Auto-notification to supervisors
- **3 Suspensions** within 30 days → Auto-recommendation for demotion
- **Active Reprimand** → Promotion blocked until lifted
- **5+ Punishments** in 30 days → Flagged as "HIGH RISK" on profile

---

## 13. GOVERNMENT BUDGET CONTROL SYSTEM

### Overview

The **City Government faction** controls how money flows to all other factions. This is the core economic system that ties all factions together.

### Revenue Flow

```
CITY REVENUE ($1,000,000 / week)
         │
         ▼
  ┌─────────────────┐
  │  GOVERNMENT      │
  │  TREASURY        │
  │  (Mayor controls)│
  └────────┬─────────┘
           │
    Mayor signs budget
           │
     ┌─────┼─────┬──────┬──────┬──────┐
     ▼     ▼     ▼      ▼      ▼      ▼
  POLICE  FIRE  HOSP  MILIT  MECH  GOV OPS
  $300K   $150K $200K  $250K  $50K   $50K
```

### Budget Process

| Step | Who | Action |
|------|-----|--------|
| 1 | System | City revenue deposited to Government treasury weekly ($1,000,000) |
| 2 | Deputy Mayor (5) | **Proposes** budget allocation — how much each faction gets |
| 3 | Department Head (4) | Can **review and comment** on the proposal |
| 4 | City Manager (6) | Can **approve** allocations up to $100,000 per faction |
| 5 | **Mayor (7)** | **MUST SIGN** all budget distributions — this is the final authority |
| 6 | System | Once signed, funds are transferred to each faction's treasury |

### Budget Rules

- **Only the Mayor** can sign and execute the final budget distribution
- The City Manager can approve individual transfers up to $100,000 without Mayor sign-off
- The Deputy Mayor can **propose** but cannot approve or execute
- All budget actions are **logged in the government audit trail**
- If the Mayor is inactive for 14+ days, the City Manager gains temporary signing authority
- Emergency funds can be unlocked by the Mayor during a declared City Emergency (releases 20% reserve)

### Budget Allocation UI Flow

1. Deputy Mayor opens **Budget Panel** in Government settings
2. Sets dollar amounts for each faction: Police $_____, Fire $_____, Hospital $_____, Military $_____, Mechanic $_____
3. Submits proposal → notification sent to City Manager and Mayor
4. City Manager reviews and can approve amounts under $100K each
5. **Mayor reviews and SIGNS** — this triggers the actual fund transfer
6. All faction leaders receive notification: "Budget allocation received: $XXX,XXX"

### Government Tax System

The Mayor can set a **tax rate** (1-10%) on all faction earnings:
- Each faction pays X% of their income to the Government treasury
- Tax rate is set by the Mayor only
- Tax revenue adds to the Government's weekly income
- All factions can see the current tax rate

---

## 14. MECHANIC CROSS-FACTION ASSIGNMENT SYSTEM

### Overview

The Mechanic Shop has a **unique ability**: it can deploy its members to other factions as dedicated mechanics. This creates a cross-faction relationship where mechanics serve other organizations.

### How It Works

1. **Request or Assignment:** Another faction's leader can request a mechanic, OR the Mechanic leadership can proactively assign
2. **Eligibility:** Only ranks 2-4 (Mechanic, Senior Mechanic, Shift Lead) can be deployed
3. **Assignment:** Service Manager (5+) opens a member's profile → "Deploy to Faction" → selects target faction → sets duration
4. **Duration:** 3, 5, or 7 days (set by Co-Owner/Owner, default 3 days)
5. **Active Deployment:** The deployed mechanic appears in both faction member lists — their home faction (Mechanic Shop) and the target faction (as "DEPLOYED MECHANIC")
6. **Recall:** Service Manager+ can recall a mechanic early by clicking "Recall" on their profile

### Deployment Details

| Setting | Who Controls | Options |
|---------|-------------|---------|
| Which member to deploy | Service Manager (5+) | Select from rank 2-4 members |
| Target faction | Service Manager (5+) | Police, Fire, Hospital, Military, Government |
| Duration | Co-Owner (6+) | 3, 5, or 7 days |
| Early recall | Service Manager (5+) | Pull mechanic back immediately |
| Payment negotiation | Co-Owner (6+) | Set daily rate the target faction pays |
| Cancel all deployments | Shop Owner (7) | Recall everyone at once |

### What the Deployed Mechanic Does

While deployed, the mechanic:
- Appears in the target faction's member list with a wrench (🔧) badge
- Can repair/maintain that faction's vehicles
- Gets paid by the target faction at the negotiated daily rate
- Still belongs to the Mechanic Shop (home faction)
- Can be punished by EITHER faction's leadership during deployment
- Returns automatically when the duration expires

### Deployment Limits

- Max **3 mechanics** deployed at the same time (per faction target)
- A mechanic can only be deployed to **one faction at a time**
- Minimum **24hr cooldown** between deployments for the same mechanic
- The Mechanic Shop must keep at least **5 members** at home (not deployed)

---

## 15. INTER-FACTION RELATIONSHIPS

### How Factions Connect

```
                    ┌──────────────┐
                    │  GOVERNMENT  │
                    │  (Controls   │
                    │   Budget)    │
                    └──────┬───────┘
                           │ Budget $$
          ┌────────┬───────┼───────┬────────┐
          ▼        ▼       ▼       ▼        ▼
      ┌───────┐ ┌──────┐ ┌─────┐ ┌──────┐ ┌────────┐
      │POLICE │ │ FIRE │ │HOSP │ │MILIT │ │MECHANIC│
      └───┬───┘ └──┬───┘ └──┬──┘ └──┬───┘ └───┬────┘
          │        │        │       │          │
          └────────┴────────┴───────┴──────────┘
                           │
                    Mechanic deploys
                    members to serve
                    other factions
```

### Faction Interaction Matrix

| From → To | Police | Fire | Hospital | Military | Government | Mechanic |
|-----------|:------:|:----:|:--------:|:--------:|:----------:|:--------:|
| **Police** | — | Mutual aid | Transport wounded | Joint ops | Reports to | Requests mechanic |
| **Fire** | Mutual aid | — | Transport wounded | — | Reports to | Requests mechanic |
| **Hospital** | Treats officers | Treats firefighters | — | Treats soldiers | Reports to | Requests mechanic |
| **Military** | Joint ops | — | Treats soldiers | — | Reports to | Requests mechanic |
| **Government** | Funds & oversees | Funds & oversees | Funds & oversees | Funds & oversees | — | Funds & oversees |
| **Mechanic** | Deploys mechanic | Deploys mechanic | Deploys mechanic | Deploys mechanic | Deploys mechanic | — |

### Alliance System (Gangs Only)

- Gangs can form **alliances** with other gangs
- Allied gangs share chat channels and cannot attack each other
- Alliance proposed by Right Hand (6+), accepted by the other gang's Right Hand+
- Max 2 active alliances per gang

### War System (Gangs Only)

- Gangs can **declare war** on other gangs
- War involves turf control — attacking and defending territory zones
- War declared by Right Hand (6+)
- War ends when one side surrenders (Leader) or after 7 days (highest turf wins)

---

## 16. FACTION BANK & ECONOMY

### Treasury

Each faction has a **treasury** (bank account) that holds faction funds.

| Source | Description |
|--------|-------------|
| Government Budget | Weekly allocation from Government (see Section 13) |
| Member Deposits | Members can deposit personal $ into faction bank |
| Faction Tax | % of member earnings auto-deducted (set by leader) |
| Service Income | Mechanic: repair fees. Hospital: treatment fees |
| Fines | Collected from punishment-related pay docks |

### Withdrawal Limits (per rank tier, daily)

| Tier | Daily Limit |
|------|-------------|
| Tier 0 (Recruit) | $0 (deposit only) |
| Tier 1 (Regular) | $100 |
| Tier 2 (Senior) | $500 |
| Tier 3 (Supervisor) | $2,000 |
| Tier 4 (Jr. Command) | $5,000 |
| Tier 5 (Sr. Command) | $10,000 |
| Tier 6 (Deputy) | Unlimited |
| Tier 7 (Leader) | Unlimited |

### Salary System

- Each rank has a **pay rate** set by the Leader
- Salaries are paid automatically every game cycle
- Default pay rates:

| Tier | Default Salary/Cycle |
|------|---------------------|
| Tier 0 | $10 |
| Tier 1 | $25 |
| Tier 2 | $50 |
| Tier 3 | $100 |
| Tier 4 | $200 |
| Tier 5 | $500 |
| Tier 6 | $1,000 |
| Tier 7 | $2,000 |

### Bonus System

Officers can grant bonuses from the faction treasury:

| Who Can Grant | Max Bonus Amount | Approval Needed? |
|--------------|-----------------|-----------------|
| Jr. Command (Tier 4) | $300 | No |
| Sr. Command (Tier 5) | $500 | No |
| Deputy (Tier 6) | $5,000 | No |
| Leader (Tier 7) | Unlimited | No |

### Transaction Log

Every financial action is logged:
- Deposits, withdrawals, salary payouts, bonuses, pay docks, inter-faction transfers
- Visible to Tier 4+ (command ranks)
- Full audit access for Tier 6+ (deputy/leader)

---

## APPENDIX A: FULL PERMISSION MATRIX (ALL FACTIONS)

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

## APPENDIX B: RANK INSIGNIA REFERENCE

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
PFF = ─       FF = ●       ENG = ●●      LT = ═
CPT = ══      BC = ★       AC = ★★       CHIEF = ★★★
```

### Hospital
```
INT = ─       NRS = +      RES = ++      ATT = +++
CR = ═        DH = ═+      MD = ★+       CMO = ★★+
```

### Government
```
INT = ─       CLK = ●      AO = ●●       SUP = ═
DH = ══       DM = ★       CM = ★★       MAYOR = ★★★
```

### Mechanic
```
APP = ─       JR = ●       MECH = ●●     SR = ●●●
LEAD = ═      MGR = ══     CO = ★        OWNER = ★★
```

### Gang
```
ASC = ─       PSP = ▼      SLD = ▼▼      ENF = ▼▼▼
LT = ◆       UB = ◆◆      RH = ★        BOSS = ★★
```
