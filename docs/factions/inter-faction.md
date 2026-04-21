# Inter-Faction Relationships

How factions connect and interact with each other.

---

## Connection Map

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

## Interaction Matrix

| From → To | Police | Fire | Hospital | Military | Government | Mechanic |
|-----------|:------:|:----:|:--------:|:--------:|:----------:|:--------:|
| **Police** | — | Mutual aid | Transport wounded | Joint ops | Reports to | Requests mechanic |
| **Fire** | Mutual aid | — | Transport wounded | — | Reports to | Requests mechanic |
| **Hospital** | Treats officers | Treats firefighters | — | Treats soldiers | Reports to | Requests mechanic |
| **Military** | Joint ops | — | Treats soldiers | — | Reports to | Requests mechanic |
| **Government** | Funds & oversees | Funds & oversees | Funds & oversees | Funds & oversees | — | Funds & oversees |
| **Mechanic** | Deploys mechanic | Deploys mechanic | Deploys mechanic | Deploys mechanic | Deploys mechanic | — |

## Key Relationships

### Government → All Factions
The Government controls the money. See [budget-control.md](government/budget-control.md).

### Mechanic → All Factions
Mechanics can be deployed to serve other factions. See [cross-faction-deployment.md](mechanic/cross-faction-deployment.md).

### Gang ↔ Gang
Gangs can form alliances or declare wars. See [gangs/actions.md](gangs/actions.md).
