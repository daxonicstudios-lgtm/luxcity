# Faction Punishment System

The punishment system is a core part of faction discipline. It creates real gameplay consequences — when a member is punished, they must **physically complete the punishment** in the game world.

**Rule: You can ONLY punish ranks BELOW yours. Never equal or above.**

---

## Punishment Types

### 1. VERBAL WARNING (Tier 2+)
- Lightest punishment
- Logged in member's record
- No gameplay effect
- 3 verbal warnings = auto-escalation to supervisor

### 2. CHAT MUTE
- **5 minutes:** Tier 2+ can issue
- **1 hour:** Tier 3+ can issue
- Member cannot send messages in faction chat during mute

### 3. EXTRA DUTY / SHIFTS (Tier 3+)
- Assigned additional tasks (patrol, guard, cleanup, etc.)
- Shows as active assignment on member's profile
- Must be completed to clear

### 4. LAPS (Tier 3+)
- Physical running punishment with checkpoint system
- Most common punishment across all factions
- 1-10 laps can be assigned
- Each lap has a defined route with checkpoints
- See [Laps Mechanic](#laps-punishment-mechanic) below

### 5. DESK/STATION DUTY (Tier 4+)
- Restricted from field activities
- Must remain at faction HQ
- Duration: 1-24 hours (game time)

### 6. SUSPENSION
- **24hr:** Tier 5+ can issue
- **7 day:** Tier 6+ can issue
- Temporarily lose rank privileges
- Cannot access faction bank
- Cannot participate in faction activities
- Still visible in member list as "SUSPENDED"

### 7. PAY DOCK (Tier 6+ only)
- Salary reduced by 50% for a set period
- Duration: 1-7 cycles

### 8. REPRIMAND (Tier 7 Leader + Tier 6 Deputy ONLY)
- **The most severe punishment short of dismissal**
- Creates a **permanent mark** on member's disciplinary record
- Blocks promotions until the reprimand is reviewed and lifted
- Visible to all officers when viewing the member's profile
- Can only be lifted by Leader or Deputy
- Logged with: date, reason, who issued it, and current status (active/lifted)

---

## Laps Punishment Mechanic

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

## Disciplinary Records

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
