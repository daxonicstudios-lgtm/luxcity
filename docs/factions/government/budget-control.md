# Government Budget Control System

The City Government controls how money flows to ALL other factions. This is the core economic system that ties all factions together.

---

## Revenue Flow

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

## Budget Process

| Step | Who | Action |
|------|-----|--------|
| 1 | System | City revenue deposited to Government treasury weekly ($1,000,000) |
| 2 | Deputy Mayor (5) | **Proposes** budget allocation — how much each faction gets |
| 3 | Department Head (4) | Can **review and comment** on the proposal |
| 4 | City Manager (6) | Can **approve** allocations up to $100,000 per faction |
| 5 | **Mayor (7)** | **MUST SIGN** all budget distributions — this is the final authority |
| 6 | System | Once signed, funds are transferred to each faction's treasury |

## Budget Rules

- **Only the Mayor** can sign and execute the final budget distribution
- The City Manager can approve individual transfers up to $100,000 without Mayor sign-off
- The Deputy Mayor can **propose** but cannot approve or execute
- All budget actions are **logged in the government audit trail**
- If the Mayor is inactive for 14+ days, the City Manager gains temporary signing authority
- Emergency funds can be unlocked by the Mayor during a declared City Emergency (releases 20% reserve)

## Budget Allocation UI Flow

1. Deputy Mayor opens **Budget Panel** in Government settings
2. Sets dollar amounts for each faction: Police $_____, Fire $_____, Hospital $_____, Military $_____, Mechanic $_____
3. Submits proposal → notification sent to City Manager and Mayor
4. City Manager reviews and can approve amounts under $100K each
5. **Mayor reviews and SIGNS** — this triggers the actual fund transfer
6. All faction leaders receive notification: "Budget allocation received: $XXX,XXX"

## Tax System

The Mayor can set a **tax rate** (1-10%) on all faction earnings:
- Each faction pays X% of their income to the Government treasury
- Tax rate is set by the Mayor only
- Tax revenue adds to the Government's weekly income
- All factions can see the current tax rate
