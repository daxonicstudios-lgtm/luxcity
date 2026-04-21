# Shared Faction Screens

These screens are used by **ALL factions**. Each is branded with the faction's color, logo, and insignia.

For the full ASCII layouts, see [screens/13-faction-panel.md](../game/) (screen IDs 13A-13Q).

---

## Screen List

| ID | Screen | Description |
|----|--------|-------------|
| 13A | Faction Browser | List of all factions with JOIN buttons |
| 13B | Faction Home | Dashboard with logo, stats, and navigation buttons |
| 13C | Member List | Paginated (10/page) with rank insignia and online status |
| 13D | Member Profile/Actions | Popup with tier-based action buttons (4 variants) |
| 13E | Assign Laps Modal | Select laps count and enter reason |
| 13F | Laps HUD Overlay | In-game overlay showing lap progress and checkpoint |
| 13G | Faction Chat | Group chat with rank insignia and timestamps |
| 13H | DM Chat | 1-on-1 messaging between members |
| 13I | Faction Bank | Treasury balance, deposit/withdraw, transaction log |
| 13J | Grant Bonus Modal | Enter amount and reason for bonus |
| 13K | Disciplinary Record | Full punishment history for a member |
| 13L | Faction Settings | Motto, recruitment, pay rates, tax, danger zone (Leader/Deputy) |
| 13M | Audit Log | Paginated log of all faction actions |
| 13Q | Reprimand Modal | Severe punishment confirmation (Leader/Deputy only) |

## Faction-Specific Screens

| ID | Screen | Faction |
|----|--------|---------|
| 13N | Government Budget Panel | Government only |
| 13O | Mechanic Deployment Panel | Mechanic only |
| 13P | Deploy Mechanic Modal | Mechanic only |

## Member Profile Action Variants

The member profile popup (13D) shows different actions based on the viewer's tier:

| Viewer Tier | Sections Shown |
|-------------|---------------|
| Tier 0-1 (Recruit/Regular) | Basic info + DM button only |
| Tier 2 (Senior) | + Verbal warning, chat mute |
| Tier 3 (Supervisor) | + Assign duty, mentor, review, laps, extra duty |
| Tier 4-5 (Command) | + Promote, demote, bonus, leave, desk duty, suspend, view record |
| Tier 6-7 (Deputy/Leader) | + Fire/dismiss, pay dock, reprimand, transfer leadership |
