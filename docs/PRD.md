**✅ Perfect. Let's build something awesome.**

I’ve created a complete **Product Requirements Document (PRD)** tailored exactly to your request:

- Dungeon Master-style clone (personal project — heavy original level replication allowed for now)
- Written in **clean, modern C + Raylib** (first target)
- Designed with **SOLID principles**, strong modularity, and **maximum portability** (Raylib → your Tiny-OS later)
- Full breakdown into **Epics → User Stories → Feature Branch Slices**
- Git workflow: feature branches, smoke + regression tests, merge gate, then continue

---

### **PROJECT NAME**: **DecaMaster** (or **Tiny Dungeon Master**)

**Tagline**: A faithful personal recreation of *Dungeon Master* in clean, portable C.

### 1. Project Vision & Goals

**Primary Goal**  
Build a faithful, playable Dungeon Master experience that runs beautifully on modern machines (Raylib) and can be ported cleanly to your Tiny-OS later.

**Key Design Principles**
- **Portability First**: Abstract all platform-specific code (rendering, input, audio, file I/O)
- **SOLID + Clean Architecture**: Single Responsibility, Dependency Inversion, modular layers
- **Personal Use Allowed**: Exact original levels for now (private repo)
- **Future-Proof**: Level editor planned from day 1 (data-driven)

**Target Platforms (in order)**
1. macOS / Windows / Linux via Raylib
2. Your Tiny-OS (pmode C, mode 13h)

---

### 2. Core Features (MVP)

- First-person 3D raycasted view (like original DM)
- Grid-based step movement + smooth turning
- 4-character party with stats, equipment, health/mana
- Real-time combat with pause
- Rune-based spell system (simplified)
- Inventory management (backpack + equipped items)
- Interactive world: doors, pressure plates, pits, teleporters, etc.
- Faithful recreation of original levels (starting with Level 1 → Hall of Champions)
- Save / Load system
- Level Editor (Phase 2)

---

### 3. Technical Architecture (Portable Design)

**Layered Structure** (very important for future Tiny-OS port)

```
core/                  ← Pure C, no Raylib
├── game/              ← Game logic, entities, combat, spells
├── world/             ← Map, levels, objects, raycasting math
├── entities/          ← Player, Party, Monsters, Items
├── ui/                ← UI panels, portraits, spell hand
├── data/              ← Level data, textures (as arrays or loaders)
├── utils/             ← Math, fixed-point, logging

platform/              ← Platform-specific implementations
├── raylib/            ← Current target
├── tinyos/            ← Future target (stubbed)
└── sdl/               ← Optional future

assets/                ← Converted to C arrays initially
```

All game logic lives in `core/`. Platform layer only handles drawing, input, and timing.

---

### 4. Epics & Feature Branch Slices

#### **Epic 1: Foundation & Raylib Setup** (1–2 days)
- Project skeleton with clean architecture
- Basic window + input abstraction
- Fixed-point math library
- Logging & debug overlay

**Feature Branches**:
1. `feat/project-setup`
2. `feat/input-abstraction`
3. `feat/fixed-point-math`

#### **Epic 2: Core Raycaster** (2–4 days)
- Textured raycasting engine
- Floor & ceiling casting
- Distance shading
- Texture array system (64x64)

**Feature Branches**:
4. `feat/raycaster-core`
5. `feat/texture-system`
6. `feat/floor-ceiling`

#### **Epic 3: World & Movement** (3–5 days)
- Grid-based map system
- Collision detection
- Step-based movement + turning
- Doors, pressure plates, triggers

**Feature Branches**:
7. `feat/map-data`
8. `feat/player-movement`
9. `feat/interactive-objects`

#### **Epic 4: Party System** (4–6 days)
- 4 characters with stats
- Portraits + health/mana bars
- Inventory + equipping

**Feature Branches**:
10. `feat/party-system`
11. `feat/inventory`
12. `feat/character-ui`

#### **Epic 5: Combat & Spells** (5–8 days)
- Monster AI
- Real-time combat
- Simplified rune spell system
- Damage, death, loot

**Feature Branches**:
13. `feat/combat-system`
14. `feat/monsters`
15. `feat/spell-system`

#### **Epic 6: Levels & Progression**
- Recreate original DM levels (data-driven)
- Multiple levels + transitions
- Save/Load

**Feature Branches**:
16. `feat/level-1-hall-of-champions`
17. `feat/save-load`
18. `feat/multiple-levels`

#### **Epic 7: Polish & Level Editor** (Later)
- Sound (once audio is ready)
- UI polish
- Level editor tool

---

### 5. Development Workflow (LLM + You)

We will follow this **exact process**:

1. I create the next feature branch description + implementation plan.
2. I write the full code for that slice.
3. I include smoke tests + regression checklist.
4. You review, test, commit & merge the branch to `main`.
5. You reply **“continue”** (or give feedback).
6. I move to the next feature branch.

This keeps everything clean, reviewable, and safe.

Let’s make **DecaMaster** something you’re really proud of. 🚀

Type **START PROJECT** when you’re ready.
