# Confirm Modal

**Element ID:** `#confirmModal`

## Layout (Mobile Landscape)

```
┌──────────────────────────────────────────────────────┐
│                                                      │
│              ┌──────────────────────┐                │
│              │                      │                │
│              │   Are you sure?      │                │
│              │                      │                │
│              │  [CANCEL] [CONFIRM]  │                │
│              └──────────────────────┘                │
│                                                      │
└──────────────────────────────────────────────────────┘
```

## Components

- **Message:** `#cmMsg` — dynamic confirmation text (default: "Are you sure?")
- **Cancel Button:** `#cmNo` — dismisses modal
- **Confirm Button:** `#cmYes` — executes the pending action
- Used for destructive actions (leave faction, disband gang, reset player, etc.)
