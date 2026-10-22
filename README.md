# Task 3: Game State, Progression, and Persistence
Builds on Task 2 (same files, upgraded). **Objective:** reliable state transitions and meaningful progression.

| Deliverable | File |
|---|---|
| Updated playable build | `index.html` + scripts in this folder |
| State diagram + edge-case checklist | [STATE_AND_TESTS.md](STATE_AND_TESTS.md) |

**Added over Task 2**
- Explicit state machine: `menu → select → playing ⇄ paused → won / lost`, restart from any end state; illegal transitions are ignored (`T` table in `game.js`).
- Progression: level select with 1-3 stars (vs par); next level unlocks after ≥1 star.
- Rules: move limit (2 x par + 3) gives a lose state; free undo.
- Persistence: only level stars (and later settings) in `localStorage` key `lumen-v1`; the game works if storage is blocked.
- Auto-pause when the tab is hidden; keys `U` undo, `R` restart, `P`/`Esc` pause.

**Quick test:** work through the checklist in STATE_AND_TESTS.md, then reload and confirm stars/unlocks persist.
