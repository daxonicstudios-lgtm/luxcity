# Main Gameplay HUD

**Element ID:** `#hud`

## Layout (Mobile Landscape)

```
┌──────────────────────────────────────────────────────┐
│ ┌──────────────┐                        ┌─────────┐ │
│ │ HEALTH ██████│                        │(MINIMAP)│ │
│ │ STAM   ██████│                        │  ⬤ you │ │
│ │ ¢ 900        │                        └─────────┘ │
│ │ ★★★☆☆        │                           06:12    │
│ ├──────────────┤                                    │
│ │ LVL 1  ░░░░░ │                                    │
│ └──────────────┘                                    │
│                                                      │
│                                                      │
│                      [PLAYER]            ☰ 😀 📱 🎒 │
│  ┌─────────┐                          ┌────┐┌────┐  │
│  │ ◉ JOY   │                          │ »» ││ ✊  │  │
│  │  STICK   │                          │SPRT││PNCH│  │
│  └─────────┘                          └────┘└────┘  │
└──────────────────────────────────────────────────────┘
```

## Components

### Top-Left Stats
- **Health Bar:** `#hpBar` — red/green gradient
- **Stamina Bar:** `#staminaBar` — green bar
- **Cash Display:** `#cashVal` — current money
- **Wanted Stars:** `#wantedStars` — 5 stars (active = gold)
- **Level/XP:** `#lvlVal` + `#xpBar` — level number and XP progress bar
- **Faction Badge:** `#factionBadge` — shows rank + faction name (if in faction)

### Top-Right
- **Minimap:** `#minimapWrap` > `#miniCanvas` — clickable, opens full map
- **Game Clock:** `#gameClock` — in-game time display
- **Speed Panel:** `#speedPanel` — shows speed when in vehicle
- **Mission Tracker:** `#missionTracker` — active mission title + objective

### Middle
- **Notification Queue:** `#notifQueue` — toast-style notifications
- **Prompt:** `#prompt` — contextual interaction prompt ("TAP ENTER")
- **Swipe Layer:** `#swipeLayer` — touch input for camera control

### Bottom-Left
- **Joystick:** `#joy` + `#knob` — virtual analog stick for movement

### Bottom-Right (Quick Buttons Row)
- **Menu:** `#btnMenu` (☰) — opens main menu
- **Emote:** `#btnEmote` (😀) — opens emote wheel
- **Phone:** `#btnPhone` (📱) — opens phone UI
- **Inventory:** `#btnInv` (🎒) — opens inventory

### Bottom-Right (Action Buttons)
- **Sprint:** `#btnSprint` — hold to run
- **Punch:** `#btnPunch` — melee attack
- **Enter Vehicle:** `#btnEnter` — shown near vehicles (hidden by default)
