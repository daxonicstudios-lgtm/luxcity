# Character Creation

**Element ID:** `#charCreate`

## Layout (Mobile Landscape)

```
┌──────────────────────────────────────────────────────┐
│                                                      │
│  ┌──────────┐  CREATE YOUR CHARACTER                 │
│  │          │                                        │
│  │  3D CHAR │  NAME  [________________]              │
│  │ PREVIEW  │  GENDER  [MALE] [FEMALE]               │
│  │  (idle   │  SKIN    ⬤ ⬤ ⬤ ⬤ ⬤ ⬤                │
│  │  anim)   │  HAIR    ▮ ▮ ▮ ▮ ▮                    │
│  │          │  HAIR CLR ⬤ ⬤ ⬤ ⬤ ⬤                  │
│  └──────────┘  TOP     ■ ■ ■ ■                       │
│                BOTTOM  ■ ■ ■ ■                       │
│                STORY   [Hustler][Street][...]         │
│                ┌──────────────────┐                  │
│                │  ENTER LUXCITY   │                  │
│                └──────────────────┘                  │
└──────────────────────────────────────────────────────┘
```

## Components

- **3D Preview:** `#ccPreview` — live rotating character model with idle animation
- **Name Input:** `#ccName` — max 16 characters
- **Name Error:** `#ccErr` — validation error display
- **Gender Select:** `#ccGender` — MALE / FEMALE toggle buttons
- **Skin Tone:** `#ccSkin` — color swatches row
- **Hair Style:** `#ccHair` — style option buttons
- **Hair Color:** `#ccHairColor` — color swatches row
- **Top Clothing:** `#ccTop` — color/style options
- **Bottom Clothing:** `#ccBottom` — color/style options
- **Backstory:** `#ccBackstory` — preset backstory options (Hustler, Street Kid, etc.)
- **Enter Button:** `#ccEnter` — confirms creation and enters game
