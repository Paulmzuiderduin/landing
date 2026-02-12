# Waterpolo Suite Roadmap

Last updated: 2026-02-12

This roadmap builds a cohesive suite of waterpolo tools with shared data, navigation, and analytics. The focus is to ship a useful scoring app first, then expand into possession/passing and video analysis.

---

## Phase 0 — Foundation (Shared Core)
**Goal:** One account, one data model, one UX system.

- Supabase auth + roles (coach / analyst)
- Shared seasons, teams, rosters
- Shared event model (shots + stats + possession events)
- Consistent navigation + design system
- Export layer (CSV / PDF) reused across apps

**Deliverable:** All future apps can reuse the same database + UI building blocks.

---

## Phase 1 — Scoring & Stats App (MVP)
**Goal:** Log match events and generate team/player stats fast.

**Core features**
- Live match event timeline
- Goals, exclusions, fouls, timeouts, turnovers, penalties
- Player attribution (cap number)
- Team stats dashboard (man-up %, man-down %, steals, blocks)
- Period summary + export

**Nice-to-have**
- Live scoreboard with timers
- Possession timer
- Auto-summaries per period

**Why now:** Highest value per effort, easy to adopt by teams.

---

## Phase 2 — Passing & Possession Map
**Goal:** Track full attacks and visualize ball movement by player and field position.

**Core features**
- Track possessions as sequences of passes
- Each pass stores:
  - From player → to player (cap number)
  - From position (x/y) → to position (x/y)
  - Timestamp, period, attack type
- Attack outcome (goal / miss / exclusion / turnover)
- Visual replay of possession (animated or step-through)
- Passing network view (nodes = players, edges = pass counts)
- Heat density of pass origins and destinations (not zone-based)

**Nice-to-have**
- Mark “key passes” and assists
- Compare lineups or quarters
- Split by transition vs set-offense

**Why second:** Builds on shotmap logic, adds tactical insight without video complexity.

---

## Phase 3 — Video Analysis (Pro)
**Goal:** Tag video and connect clips to events.

**Core features**
- Upload video or connect storage
- Tag events on a timeline (shot, goal, exclusion, pass)
- Link events to data from Shotmap/Stats/Passing
- Clip export + share links

**Nice-to-have**
- Auto‑sync with timestamped data
- Player highlight reels
- Coach comments + annotation

**Why third:** Highest complexity, strongest premium feature.

---

## Cross‑App Enhancements (Ongoing)
- Player report cards (season comparisons)
- Team trends dashboard
- Advanced filters (lineups, opponent, match phases)
- Subscription tiers (storage + advanced analytics)

---

## Data Model Summary (High-Level)
- **Seasons** → **Teams** → **Players**
- **Matches** with **Events** (shots, goals, exclusions, passes)
- **Possessions** with ordered **Passes**
- **Video tags** reference event IDs

---

If you want this turned into a visual roadmap or used on the landing page, tell me the style (minimal, sport‑tech, or presentation). 
