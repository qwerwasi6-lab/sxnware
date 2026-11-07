# SxnWare

External Counter-Strike cheat with a VACNet-aware humanization stack, a standalone pre-launcher, and a full overlay menu. SxnWare is built around quiet behavior: configurable reaction windows, recoil drift, rate caps, and per-feature control over keybind, activation mode, and color.

---

## Quick Start

1. Run the SxnWare pre-launcher.
2. Complete the first-run wizard: language, DPI scale, and interface colors.
3. Launch Counter-Strike.
4. Open the overlay with your configured menu key.
5. Tune a profile, save it as a config, and load it between sessions.

---

## Core Controls

Every feature row supports the same control surface:

| Control | Options |
|---|---|
| Keybind | Any supported input |
| Activation | Hold / Toggle / Always Active |
| Color | Per-feature color picker |
| Master Switch | Per-module enable/disable |

---

## Menu Tree

| Menu | Tabs |
|---|---|
| AimBot | Legit, Triggerbot |
| Visuals | Players, Items, Projectiles, Bomb, Radar, Effects, Crosshair |
| Misc | General, Overlay, Movement, Walk Bot, Grenades, Scripts, Configs |

---

## Pre-Launcher

SxnWare ships with a separate launcher that runs before the overlay attaches.

- First-run wizard with English / Русский language selection.
- Applies DPI scale and interface color profile.
- Keeps launcher state separate from in-game menu state.
- Loads the external overlay after the game window is available.
- Stores profile and config paths outside the game directory.

---

## AimBot

### Legit

Humanized aim assist with a configurable reaction model. Defaults shown from the shipped profile.

| Setting | Default |
|---|---|
| Master Switch | On |
| Key | `C` |
| Checks | None |
| Hitboxes | All |
| FOV | Configurable |
| Humanizer Profile | Custom |
| Amount | 65% |
| Smoothing | 8 |
| Reaction Min | 130 ms |
| Reaction Max | 235 ms |
| Curve | 0.55 |
| Overshoot Chance | 18% |
| Overshoot Amount | 0.00 |
| Jitter | 0.22 |
| Deadzone | 0.25° |
| Motion | Configurable |
| Behavior | Configurable |
| Multi-Point | On |
| Prediction | On |
| Lethal Only | On |

**Recoil Control**

| Setting | Default |
|---|---|
| RCS | On |

**Penetration**

| Setting | Default |
|---|---|
| Only Visible | On |
| Min Damage | 65 |
| Damage Override | On |

### Triggerbot

Triggerbot core with delay randomization, outlier handling, and penetration limits.

| Setting | Default |
|---|---|
| Master Switch | On |
| Key | `C` |
| Checks | None |
| Seed Type | None |
| Hitboxes | Head, Body |
| Hitchance | 55% |
| Auto Stop | On |
| Shot Timing | Configurable |
| Predictive | On |
| Lethal Only | On |
| Delay Before | 70 ms |
| Randomize | 35 ms |
| Outlier Chance | 8.0% |
| Outlier Delay | 90 ms |
| Delay After | 220 ms |
| Only Visible | On |
| Min Damage | 90 |
| Damage Override | On |

---

## VACNet Shield

The stealth layer is exposed under `Misc → General → VACNet Shield`.

| Setting | Purpose |
|---|---|
| Enable Shield | Master switch for behavioral caps |
| Reaction Delay Gate | Prevents instant trigger after visibility |
| Block Wallbang Trigger | Blocks trigger through non-visible surfaces |
| Headshot Ratio Cap | Limits headshot rate |
| Hit Rate Cap | Limits overall hit rate |
| Shot Rate Floor | Enforces a minimum interval between shots |
| RCS Residual Drift | Leaves human-like recoil error instead of perfect compensation |

---

## Visuals

### Players

- Enable Player ESP
- Legit Sync
- Show Name
- Show Weapon
- Health Bar
- Armor Bar
- Info Flags
- Chams
- Chams Visible
- Chams Occluded
- Bounding Box: Show Box, Style, Corner Length, Background Fill
- Skeleton & Hitboxes: Show Skeleton, Head Circle, View Line, Offscreen Arrows, Threat Hitboxes, Sound ESP

### Items

- Enable Item ESP
- Max Distance: `40`
- Show Icon
- Show Item Name
- Filters: Rifles, SMGs, Snipers, Pistols, Grenades, Utility

### Projectiles

- Enable Projectiles
- Display Mode: Indicator
- Show Icon
- Effect Timer Ring
- Inferno Bounds
- Colors: HE Grenade, Flashbang, Smoke, Molotov, Decoy
- Indicator: Timer Full, Timer Low, Indicator Background
- Inferno Gradient: Width `34 px`, Opacity `45%`

### Bomb

- Enable Bomb ESP
- Display Mode: Indicator
- Show Planter
- Show Carrier
- World Timer Ring
- Bomb Info Panel
- Safe Zone: Baked Contour

### Radar

- Overlay Enemy Markers
- Player Names
- Player Health
- Player Armor
- Player Weapon
- Player Style: Enemy Marker, View Direction, Status Text, Marker Scale, Text Outline
- Radar Grenades: Grenade Markers, Grenade Trajectories, Grenade Zones

### Effects

- Enable Bullet Tracers
- World Hitmarker
- Hit Sound
- Enable Visual No Flash
- Enable Visual No Smoke

### Crosshair

- Enable Crosshair
- Draw Dot
- Draw Lines
- Thickness: `1.00`
- Draw Outline
- Primary Color
- Penetration Indicator

---

## Misc

### General

- Auto Accept Match
- VACNet Shield
- Game Action Binds: Attack `M1`, Secondary Attack `M2`, Use `E`, Reload Weapon `R`, Buy Menu `B`, Reset
- Game Movement Binds: Forward `W`, Back `S`
- Support: Diagnostic Report Save, Logs Open, First-run Guide Show

### Overlay

- OBS Bypass
- Show Watermark
- Show Spectators
- Show Event Log
- Show Active Binds
- Show Bomb Info

### Movement

- Enable Bunny Hop
- Enable Edge Jump

### Walk Bot

- Enable Walk Bot
- Routes: Random Points
- Hunt Enemies
- Turn Camera
- Break Obstacles
- Combat: Own Aim, Autofire (Triggerbot Settings), React To Hits
- Route Display: Show Route, Show Nav Mesh, Recorded Routes
- Round: Auto Buy, Auto Reload
- Match: Auto Rejoin, Auto Disconnect

### Grenades

- Lineup Helper
- Lineup Aim Assist
- Trajectory Preview
- Grenade Assist: Enemy Aim Assist

### Scripts

- Lua script import
- Open script folder
- Scripts are disabled until imported
- Empty state: `No scripts`

### Configs

- New config
- Import
- Open folder
- Change folder
- Save
- Empty state: `No folder selected`

---

## Interface and Engine

### Interface

| Setting | Default |
|---|---|
| Language | English |
| DPI Scale | 100% |
| Interface Colors | Custom |

### Engine

| Setting | Default |
|---|---|
| FPS Limiter | On |
| GPU Effects | On |
| CPU Priority | Balanced |
| GPU Priority | Game First |

---

## Config Workflow

1. Open `Misc → Configs`.
2. Choose a config folder.
3. Create a new config name.
4. Tune modules.
5. Save.
6. Use `Import` to load existing profiles.
7. Use `Change folder` to move the profile library.

Configs are intentionally portable and stored outside the game directory.

---

## Script Workflow

1. Open `Misc → Scripts`.
2. Use `Import` to add a `.lua` script.
3. Use `Open folder` to inspect the active script directory.
4. Scripts remain inert until loaded.

---

## Support

- `Diagnostic Report → Save`
- `Logs → Open`
- `First-run Guide → Show`

The diagnostic report captures the active profile, module states, and environment details needed to reproduce configuration issues.

---

## Design Notes

- External overlay architecture keeps the menu separate from the target process.
- Humanizer values are per-profile and survive config export/import.
- Every module exposes color, keybind, and activation mode.
- VACNet Shield is intentionally layered: reaction gate, wallbang block, headshot cap, hit-rate cap, shot-rate floor, and RCS residual drift.
- Triggerbot delays are randomized with an outlier path instead of fixed timing.
- The pre-launcher owns first-run setup so the overlay starts clean.

---

## Status

SxnWare is an external, pre-launcher-driven cheat with a full humanization stack, modular ESP, movement automation, grenade helpers, Lua scripting, and portable configs.
