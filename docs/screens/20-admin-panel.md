# Admin Panel

**Element ID:** `#adminPanel`

## Layout (Mobile Landscape)

```
┌──────────────────────────────────────────────────────┐
│  ┌────────────────────────────────────────────────┐  │
│  │ // ADMIN        [GOD MODE]                 [X] │  │
│  │ [PLAYER] [FACTIONS] [MEMBERS] [WORLD] [QUICK]  │  │
│  │ ┌──────────────────────────────────────────┐   │  │
│  │ │  CASH  [___10000___] [SET]               │   │  │
│  │ │  HP    [___100_____] [SET]               │   │  │
│  │ │  MAX HP[___100_____] [SET]               │   │  │
│  │ │  LEVEL [___5_______] [SET]               │   │  │
│  │ │  XP    [___250_____] [SET]               │   │  │
│  │ │  FACTION [▼ Select ] [JOIN]              │   │  │
│  │ └──────────────────────────────────────────┘   │  │
│  └────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────┘
```

## Components

- **Header:** "// ADMIN"
- **God Mode Toggle:** `#adminGodBtn` — invincibility toggle
- **Close Button:** `#adminClose`
- **Section Tabs:** `#adminSections` — PLAYER, FACTIONS, MEMBERS, WORLD, QUICK
- **Body:** `#adminBody` — dynamic content per section

### Tab: PLAYER
- Cash: `#adCash` + `#adCashSet`
- HP: `#adHp` + `#adHpSet`
- Max HP: `#adMaxHp` + `#adMaxHpSet`
- Level: `#adLvl` + `#adLvlSet`
- XP: `#adXp` + `#adXpSet`
- Faction join: `#adJoinFaction` + `#adJoinBtn`
- Rank set: `#adSetRank` + `#adRankBtn`
- Force leave: `#adLeaveBtn`

### Tab: FACTIONS
- Create free gang: `#adCreateGangFree`

### Tab: MEMBERS
- Filter by faction: `#adMemFaction`
- Member list: `#adMemList`

### Tab: WORLD
- Teleport: `#adTpX`, `#adTpZ`, `#adTpGo`
- Current position: `#adPlayerPos`

### Tab: QUICK
- Full Heal: `#adHealFull`
- Add Cash: `#adAddCash` (+$10,000)
- Level Up x10: `#adLvlUp`
- Reset Player: `#adResetPlayer`
- Fill All NPCs: `#adFillAll`
- Clear All NPCs: `#adClearAll`
