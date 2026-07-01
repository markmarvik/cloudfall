# Cloudfall

**Cloudfall** is an FTL-inspired post-apocalyptic airship roguelike set in a Venus-like Earth where survivors live on improvised airships in the clouds.

> Browser-based • Retro pixel art • Real-time with pause combat • Dynamic wind & altitude mechanics

## Vision

After a vengeful nation detonated nuclear devices deep into Earth’s core, the atmosphere became dense, hot, and toxic (Venus-like). The surface is uninhabitable due to radiation, extreme heat, and mutated life. Humanity now survives on patchwork airships drifting in the clouds.

You manage one such airship — juggling crew, repairing gasbags mid-battle, adapting to changing wind currents, and choosing when to climb or descend into more dangerous atmospheric layers. Your ultimate goal: track down and destroy the heavily defended floating fortress of the **Core Dominion** — the faction responsible for the apocalypse.

## Current Status: MVP in Development

We are currently building the **Minimum Viable Product** focused on delivering the core fantasy:

- One playable airship
- Real-time-with-pause combat
- Basic crew & system management
- Simple sky map with wind
- 2–3 enemy types + one boss

## MVP Features

### Core Systems
- **Gasbags / Lift** – Primary buoyancy. Damage causes altitude loss and leaks.
- **Gasbag Fillers** – Pumps/heaters for fine altitude control.
- **Engines / Propellers** – Movement and maneuvering against wind.
- **Weapon Platforms** – Cannons, harpoons, point defense.
- **Bridge** – Command, sensors, targeting.
- **Crew Quarters (Bunks)** – Morale and fatigue recovery.
- **Kitchen** – Food preparation.
- **Cargo Hold** – Resources and loot.

### Gameplay Systems
- **Real-time with Pause Combat** (Hardcore mode available with no pause)
- **Vertical Movement in Battle** – Change altitude mid-fight to expose different gasbags or escape storms.
- **Dynamic Wind Currents** on an open sky map
- **Atmospheric Layers** with different hazards (storms, ice razors, toxic clouds)
- **FTL-style Ship Schematic** view with visible damage, fires, and gas leaks
- **Side-view Battle Screen** showing both ships
- **Crew Management** – Assign individual crew to stations (FTL style)
- **Resource Management** – Scrap, fuel, food, ammo
- **Basic Upgrades & Repairs** using scrap

### Content (MVP)
- 1 starting airship layout
- 2–3 distinct enemy types + 1 boss encounter
- Simple floating trading post / merchant
- Basic procedural encounters and events
- Save / Load system

## Tech Stack

- **Phaser 3** (recommended) – Scene management, sprites, input (mouse + touch), Arcade physics
- HTML5 + modern web standards
- WebP + sprite atlases for assets
- Responsive design (desktop + mobile browsers)
- PWA capable (installable, offline saves via IndexedDB)

## Art Direction

- Retro pixel art with strong steampunk / dieselpunk lean
- Consistent orange-brown Venus-like color palette
- Improvised, patchwork, battle-damaged aesthetic
- All art created or heavily iterated using AI tools + manual polish

## Project Structure (Planned)

```
cloudfall/
├── src/
│   ├── scenes/          # Phaser scenes (Boot, Preload, Map, Battle, ShipView, Merchant)
│   ├── entities/        # Ship, Crew, Enemy, Projectile, etc.
│   ├── systems/         # Combat, Damage, Wind, Altitude, CrewAI
│   └── ui/              # HUD, Pause menu, Targeting, etc.
├── assets/
│   ├── images/          # WebP + sprite sheets
│   └── data/            # JSON for ship layouts, enemy stats
├── docs/
│   └── game-plan.md   # Full Game Plan Document
├── index.html
├── package.json
└── README.md
```

## Getting Started (Development)

```bash
# Clone the repo
git clone https://github.com/markmarvik/cloudfall.git
cd cloudfall

# Install dependencies (when set up)
npm install

# Run local dev server (Phaser + Vite or similar)
npm run dev
```

Open `http://localhost:5173` (or configured port) in your browser.

## Roadmap

### MVP (Current Focus)
- [ ] Core combat loop (real-time + pause)
- [ ] Ship schematic with damage & crew assignment
- [ ] Basic enemy AI and 2–3 enemy types
- [ ] Simple sky map with wind currents
- [ ] Merchant / trading post
- [ ] Save system
- [ ] Responsive UI (desktop + mobile)

### Post-MVP
- More ship variants and visual customization
- Deeper crew skills and morale
- Atmospheric hazards and layer-specific events
- Meta-progression between runs
- More enemy types and the Enemy Fortress assault
- Full art pass and sound design
- Ad integration for free-to-play launch

## Contributing

This project is in early development. Contributions, ideas, and feedback are very welcome!

1. Fork the repo
2. Create a feature branch
3. Submit a Pull Request

Please check the [Game Plan Document](docs/game-plan.md) (when available) for detailed design decisions.

## License

MIT License – feel free to use and modify for personal or commercial projects.

---

**Built with** ❤️ by Mark using Grok

*"The sky is no longer the limit. It’s the only thing left."*