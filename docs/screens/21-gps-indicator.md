# GPS Indicator

**Element ID:** `#gpsIndicator`

## Layout (Mobile Landscape)

```
┌──────────────────────────────────────────────────────┐
│                  ┌─────────────────┐                 │
│                  │ → 24/7 Mart 85m │                 │
│                  └─────────────────┘                 │
│                                                      │
│                    (gameplay...)                      │
│                                                      │
└──────────────────────────────────────────────────────┘
```

## Components

- **Destination Name:** `#gpsDest` — name of the target POI
- **Distance:** `#gpsDist` — live-updating distance to destination
- Appears at top-center when GPS navigation is active
- Auto-hides when player reaches destination
