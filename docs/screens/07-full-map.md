# Full Map

**Element ID:** `#fullMap`

## Layout (Mobile Landscape)

```
┌──────────────────────────────────────────────────────┐
│  ┌────────────────────────────────────────────────┐  │
│  │ // MAP                                     [X] │  │
│  │ ┌────────────────────────────┐  LEGEND:        │  │
│  │ │                            │  ■ Shops        │  │
│  │ │     MAP CANVAS             │  ■ Missions     │  │
│  │ │     ⬤ YOU ARE HERE         │  ■ ATM          │  │
│  │ │     ⊕ Selected POI         │  ■ Garage       │  │
│  │ │                            │                 │  │
│  │ └────────────────────────────┘  YOUR LOCATION  │  │
│  │   Selected: 24/7 Mart  ─ 120m                  │  │
│  │              [SET GPS]  [CANCEL]                │  │
│  └────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────┘
```

## Components

- **Close Button:** `#fullMapClose`
- **Map Canvas:** `#fullMapCanvas` — interactive map with POI markers
- **Legend:** `#fullMapLegend` — color-coded POI types
- **Location Label:** `#fullMapLoc` — "YOUR LOCATION"
- **Selected POI:** `#fullMapSelected` — name of tapped POI
- **Distance:** `#fullMapDist` — distance to selected POI
- **Set GPS Button:** `#fullMapNavBtn` — starts GPS navigation to POI
- **Cancel GPS Button:** `#fullMapNavCancel` — cancels active navigation
