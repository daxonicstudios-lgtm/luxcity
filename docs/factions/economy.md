# Faction Economy & Banking

All faction finances use **$ (dollar)**.

---

## Treasury

Each faction has a **treasury** (bank account) that holds faction funds.

| Source | Description |
|--------|-------------|
| Government Budget | Weekly allocation from Government (see [budget-control](government/budget-control.md)) |
| Member Deposits | Members can deposit personal $ into faction bank |
| Faction Tax | % of member earnings auto-deducted (set by leader) |
| Service Income | Mechanic: repair fees. Hospital: treatment fees |
| Fines | Collected from punishment-related pay docks |

---

## Withdrawal Limits (per rank tier, daily)

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

---

## Salary System

- Each rank has a **pay rate** set by the Leader
- Salaries are paid automatically every game cycle

### Default Pay Rates

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

---

## Bonus System

Officers can grant bonuses from the faction treasury:

| Who Can Grant | Max Bonus Amount | Approval Needed? |
|--------------|-----------------|-----------------|
| Jr. Command (Tier 4) | $300 | No |
| Sr. Command (Tier 5) | $500 | No |
| Deputy (Tier 6) | $5,000 | No |
| Leader (Tier 7) | Unlimited | No |

---

## Transaction Log

Every financial action is logged:
- Deposits, withdrawals, salary payouts, bonuses, pay docks, inter-faction transfers
- Visible to Tier 4+ (command ranks)
- Full audit access for Tier 6+ (deputy/leader)
