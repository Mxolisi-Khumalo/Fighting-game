# NEON COMBAT: HYPER EDITION

A browser-based, Street-Fighter-style 2D fighting game built entirely in a **single HTML file** — no build step, no dependencies, no assets to download. HTML5 Canvas for rendering, vanilla JavaScript for a frame-based combat engine, and the WebAudio API for fully synthesized sound. Just open the file and fight.

![Neon Combat](preview.png)

## Features

- **6 unique fighters**, each a distinct archetype with its own stats, silhouette, Special move, and Super:
  | Fighter | Archetype | Special | Super |
  |---------|-----------|---------|-------|
  | **SHADOW** | Ninja (balanced) | Shuriken volley | Shadow Barrage (teleport multi-slash) |
  | **BLAZE** | Rushdown (glass cannon) | Fireball | Inferno Wave |
  | **TITAN** | Grappler (tank) | Seismic Pound | Meteor Crush (armored) |
  | **FROST** | Defensive/zoner | Ice Lance (freezes) | Absolute Zero |
  | **VOLT** | Speedster | Thunder Dash | Chain Lightning |
  | **NOVA** | Zoner | Plasma Orb | Photon Beam (full-screen laser) |

- **Real fighting-game engine** running at a fixed 60 Hz timestep:
  - Startup / active / recovery frame data per move
  - **Blocking** (hold back) with high/low guard, chip damage, and block-stun
  - **Crouching** with low attacks and low/overhead mix-ups
  - **Combos** via cancels (chain Light → Heavy → Special → Super) with an on-screen hit counter
  - **Throws** (Light + Heavy together), **dashing** (double-tap), and jump attacks
  - Hit-stop (impact freeze), knockback, launchers, and knockdowns
- **Super meter** built by attacking, taking damage, and advancing — spend it on a character's Super.
- **Smart CPU opponent** with Easy / Normal / Hard difficulty: spacing, blocking, anti-airs, punishes, and meter usage.
- **Local 2-player** mode on one keyboard.
- **Best-of-3 rounds** with a round timer, KO / TIME / PERFECT announcements, and screen shake / flash / particle FX.
- **Synthesized audio** — SFX and a looping soundtrack generated in-browser (mute toggle, top-right).
- **Animated neon-city backdrop** with parallax buildings, flickering windows, and a perspective grid.

## Controls

| Action | Player 1 | Player 2 |
|--------|----------|----------|
| Move | `A` / `D` | `←` / `→` |
| Jump | `W` | `↑` |
| Crouch | `S` | `↓` |
| Light attack | `F` | `K` |
| Heavy attack | `G` | `L` |
| Special | `E` | `O` |
| Super (needs full meter) | `R` | `I` |
| Throw | `F` + `G` | `K` + `L` |
| Block | hold *back* (away from opponent) | hold *back* |
| Dash | double-tap a direction | double-tap a direction |
| Pause | `Esc` | `Esc` |

**Combo tip:** cancel a connected normal into a Special or Super — e.g. `F → G → E` — to rack up hits.

## Getting Started

Clone the repository:

```bash
git clone https://github.com/Mxolisi-Khumalo/Fighting-game.git
```

Then just open `fighting_game.html` in any modern browser. That's it — no server or install required.

## Project Structure

```
Fighting-game/
├── fighting_game.html   # The entire game (HTML + CSS + JS in one file)
├── preview.png          # Screenshot (optional)
└── README.md
```

## Technologies

- **HTML5 Canvas** — rendering, characters, effects
- **Vanilla JavaScript** — frame-based combat state machine, AI, game flow
- **WebAudio API** — procedurally generated sound effects and music
- **CSS3** — HUD, menus, and animated UI
