# Cloudfall

**An FTL-inspired Post-Apocalyptic Airship Roguelike**

> Browser-based • Retro Pixel Art • Real-time with Pause Combat • Dynamic Wind & Altitude Mechanics

Cloudfall is a roguelike where you manage an improvised airship in a Venus-like post-apocalyptic Earth. The atmosphere became dense and toxic after a vengeful nation detonated nuclear devices deep into the planet’s core. Survivors now live in the clouds on patchwork airships.

Your goal: level up your ship and crew, survive escalating threats, and eventually destroy the heavily defended floating fortress of the **Core Dominion** — the faction that caused the apocalypse.

---

## Table of Contents

- [Vision & Setting](#vision--setting)
- [Core Gameplay Loop](#core-gameplay-loop)
- [MVP Scope](#mvp-scope)
- [Key Mechanics](#key-mechanics)
  - [Ship Systems](#ship-systems)
  - [Altitude & Atmospheric Layers](#altitude--atmospheric-layers)
  - [Combat](#combat)
  - [Crew](#crew)
  - [Map & Travel](#map--travel)
- [User Interface](#user-interface)
- [Art Direction & Assets](#art-direction--assets)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Roadmap](#roadmap)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

---

## Vision & Setting

### The Apocalypse
A vengeful nation (later known as the **Core Dominion**) prepared for decades and then detonated multiple nuclear devices deep into Earth’s mantle and core. This triggered massive, sustained volcanic activity. The sky filled with ash, sulfur, water vapor, and greenhouse gases, turning the atmosphere into a thick, Venus-like blanket: dense, hot, corrosive, and almost opaque.

### The World Today
- **Surface**: Extreme heat, toxic gases, high radiation. Limited mutated life exists in pockets.
- **Atmosphere**: Much denser than before — this actually makes buoyancy easier for airships.
- **Survivors**: Scattered floating communities living on improvised airships of every shape and size (repurposed zeppelin parts, shipping containers, old aircraft fuselages, fabric envelopes, etc.).

### The Enemy
The **Core Dominion** still controls the most powerful and heavily defended floating structure in the sky — their fortified citadel (the "Enemy Fortress"). Many believe they are still pursuing total control.

---

## Core Gameplay Loop

Cloudfall is a **roguelike** with meta-progression.

**Typical Run**:
1. Start with a basic airship and small crew
2. Explore an open sky map with dynamic wind currents
3. Visit points of interest (wrecks, floating cities, enemy outposts)
4. Manage resources, repair your ship, assign crew
5. Fight escalating Core Dominion patrols and environmental hazards
6. Grow stronger through upgrades and experience
7. Eventually hunt and assault the Enemy Fortress

**Escalation** comes from:
- Time passing (global threat level rises)
- Player actions (visiting certain sites or destroying patrols increases "Heat")
- Map progression (certain regions are naturally more dangerous)

Death is permanent for that run, but meta-progression (new starting parts, codex entries, cosmetics) carries over.

---

## MVP Scope

### What’s In Scope for MVP
- One starting airship layout with all core systems
- Real-time-with-pause combat against 2–3 enemy types + 1 boss
- Side-view battle screen with visible damage and basic vertical movement
- Simple open sky map with wind currents
- One floating trading post / merchant
- Basic crew assignment (FTL-style)
- Simple upgrade & repair loop
- Save / Load system
- Responsive UI (desktop + mobile)

### What’s Out of Scope for MVP
- Multiple ship visual variants
- Deep crew skills & morale
- Full atmospheric hazard events
- Meta-progression between runs
- Sound design
- The full Enemy Fortress assault

---

## Key Mechanics

### Ship Systems

| System              | Primary Function                          | Combat / Risk Notes                                      |
|---------------------|-------------------------------------------|----------------------------------------------------------|
| **Gasbags / Lift**     | Main buoyancy and altitude control       | Tears, leaks, and fires are critical. Multiple gasbags allow redundancy. |
| **Gasbag Fillers**     | Pumps, heaters, chemical systems         | Fine altitude tuning. Overpressure can cause explosions. |
| **Engines / Propellers** | Forward thrust and maneuvering          | Speed and dodge capability. Heavily affected by wind.   |
| **Weapon Platforms**   | Cannons, harpoons, point-defense         | Offense and boarding. Exposed crew when firing.         |
| **Bridge**             | Command, sensors, targeting              | If destroyed, lose manual control and pause advantage.  |
| **Bunks / Quarters**   | Crew rest and morale recovery            | Fires and gas leaks here cause rapid morale loss.       |
| **Kitchen**            | Food preparation                         | Fire hazard. Running out of food collapses morale.      |
| **Cargo Hold**         | Storage for resources and loot           | Direct hits can destroy valuable resources.             |

### Altitude & Atmospheric Layers

Altitude is a meaningful strategic layer with real trade-offs.

| Layer              | Hazards & Characteristics                                      |
|--------------------|----------------------------------------------------------------|
| **Low / Storm**       | Heavy wind storms, toxic clouds, possible ground anti-air, better loot |
| **Mid (Habitable)**   | Balanced. Default operating altitude. Floating cities common   |
| **High / Razor**      | Ice razor storms (tears gasbags), extreme cold, stronger winds |
| **Extreme High**      | Severe cold, oxygen issues, rare electrical phenomena          |

Climbing or descending is a constant decision. Gasbag damage can force unplanned altitude changes — a major source of tension.

### Combat

- **Real-time with Pause** (classic FTL tension)
- **Hardcore Mode**: No pause option for maximum difficulty
- **Unique Twist**: **Vertical movement during combat**. You can order the ship to climb or descend mid-fight. This changes which gasbags are exposed, affects weapon angles, and can move you into or out of storm layers.
- Side-view battle screen (your ship on left, enemy on right)
- Visible damage states, fires, gas leaks, and crew movement

### Crew

FTL-style individual crew members.
- Assign crew to stations (Weapons, Engines, Repair, Bridge, etc.)
- Crew can be injured or killed
- Gain experience over time
- Recruit replacements at floating cities
- Morale, fatigue, and hunger matter

### Map & Travel

- More open than FTL’s node system
- Dynamic wind currents that move across the map
- Player must adapt heading and altitude to make efficient progress
- Travel takes time (you see your ship moving)
- Random/semi-random events can trigger while traveling

---

## User Interface

The UI should feel very familiar to FTL players but adapted for airships and verticality.

### Primary Views (MVP)

- **Ship Schematic / Interior View**: Detailed side-view schematic showing gasbags, gondola compartments, crew positions, damage, fires, and gas leaks. Click to assign crew or prioritize repairs.
- **Battle Screen**: Side-by-side view of your airship and enemy ship. Both can change altitude. Projectiles, explosions, and system damage visible.
- **Sky Map / Travel View**: Open map showing wind currents, points of interest, and your ship’s position. Altitude controls.
- **Floating City / Merchant**: Trading, hiring crew, buying supplies and upgrades.
- **Crew & Upgrade Screens**: Assign crew, view skills, spend scrap on improvements.

All screens must be fully responsive and touch-friendly.

---

## Art Direction & Assets

**Style**: Retro pixel art with a strong steampunk / dieselpunk lean.

**Color Palette**: Dominated by oranges, deep reds, browns, and muted metals against sickly orange-brown skies.

**Aesthetic**: Improvised, patchwork, lived-in, and battle-damaged.

**Asset Strategy**:
- Primary formats: WebP + sprite atlases
- Avoid heavy use of GIFs (use sprite sheet animations instead)
- Procedural elements where possible (clouds, lightning, gas leaks, fire, damage decals)
- All concept art and assets created or heavily iterated using Grok Imagine

We already have several high-quality concept pieces:
- Player airship variants (scout, heavy gunship, etc.)
- Core Dominion enemy ships
- Ice razor storm hazard scene
- Full reference sheet with multiple designs

---

## Tech Stack

**Recommended**: **Phaser 3**

Reasons:
- Excellent scene management and sprite handling
- Unified input (mouse + touch + keyboard)
- Arcade physics (sufficient for this game)
- Proven web performance
- Faster development than pure vanilla Canvas while still allowing deep optimization

**Other Technologies**:
- HTML5 + modern web standards
- Responsive design (desktop-first but mobile friendly)
- IndexedDB for local saves (PWA capable)
- WebP + texture atlases for performance

**Performance Target**: Smooth 60 FPS on mid-range phones and older laptops, with graceful degradation.

---

## Project Structure (Planned)

```
cloudfall/
├── src/
│   ├── scenes/              # Game scenes (Map, Battle, ShipView, Merchant, etc.)
│   ├── entities/            # Ship, CrewMember, EnemyShip, Projectile
│   ├── systems/             # CombatSystem, DamageSystem, WindSystem, AltitudeSystem
│   ├── ui/                  # HUD components, menus, targeting
│   └── data/                # JSON configs for ships, enemies, events
├── assets/
│   ├── images/              # WebP files + sprite sheets
│   └── data/                # Additional data files
├── docs/
│   └── game-plan.md       # Full detailed Game Plan Document
├── index.html
├── package.json
└── README.md
```

---

## Roadmap

### Phase 1: MVP (Current Focus)
- [ ] Core real-time + pause combat loop
- [ ] Ship schematic view with damage visualization and crew assignment
- [ ] 2–3 enemy types + 1 boss with basic AI
- [ ] Simple sky map with dynamic wind currents
- [ ] Basic merchant / trading post
- [ ] Save / Load system (IndexedDB)
- [ ] Responsive UI (desktop + mobile touch)
- [ ] Initial art integration (player ship + enemies)

### Phase 2: Content & Polish
- More enemy variety and behaviors
- Atmospheric hazards and layer-specific events
- Deeper crew mechanics (skills, morale, fatigue)
- Multiple ship visual variants
- Meta-progression system
- Sound effects and basic music

### Phase 3: Full Game
- Enemy Fortress assault (multi-phase boss fight)
- More ship types and deep customization
- Full event system and procedural generation
- Ad integration + free-to-play monetization
- Performance optimization and mobile polish

---

## Getting Started (Development)

```bash
git clone https://github.com/markmarvik/cloudfall.git
cd cloudfall

# When the project is set up:
# npm install
# npm run dev
```

---

## Contributing

This project is in very early development. All contributions, ideas, feedback, and concept art are welcome!

Please read the detailed **[Game Plan Document](docs/game-plan.md)** (to be added) before making large changes.

---

## License

MIT License

---

**Built with ❤️ by Mark** using Grok

*"The sky is no longer the limit. It’s the only thing left."*