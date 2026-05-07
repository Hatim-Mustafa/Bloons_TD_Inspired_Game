# Bloons TD Inspired Game

A C++/SFML tower defense game inspired by Bloons TD, built as a DSA-focused project.  
The project includes tower placement, wave-based enemies, upgrades, targeting modes, and smart enemy pathing.

## Overview

This game is implemented primarily in a single source file (`main.cpp`) and demonstrates:
- Object-oriented game architecture (`GameManager`, `Tower`, `Enemy`, `Player`, `Map`, `Shop`)
- Data structures such as linked structures, stacks, vectors, and priority-like path expansion
- Pathfinding logic for enemy rerouting around tower threat zones
- Basic UI interactions for placing and upgrading towers

## Features

- **Wave system** with multiple enemy types (Red, Blue, Green)
- **Tower placement** by dragging from the shop area to valid map tiles
- **Tower upgrades** via a branching upgrade tree
- **Targeting modes**:
  - First Enemy
  - Strongest Enemy
  - Fastest Enemy
- **Projectile combat** and health/money economy
- **Win/lose states** with end overlays

## Gameplay

1. Launch the game.
2. Drag a tower from the shop panel and place it on a buildable tile.
3. Click placed towers to:
   - Open **Upgrade** options
   - Change targeting **Mode**
4. Survive all waves before player health reaches zero.

### Controls

- **Left Click (shop tower):** Start tower drag
- **Release Left Click:** Drop tower on map
- **Left Click (placed tower):** Select tower
- **Left Click (Upgrade / Mode UI):** Upgrade tower or change targeting

## Tech Stack

- **Language:** C++
- **Graphics/Windowing:** SFML 2.6.x
- **IDE/Build:** Visual Studio 2022 (`DSProj.sln`, `DSProj.vcxproj`)

## Project Structure

```text
Bloons_TD_Inspired_Game/
├── main.cpp
├── DSProj.sln
├── DSProj.vcxproj
├── README.md
├── uml_diagrams.html
└── assets (.png/.ttf files in repo root)
```

## Build & Run (Visual Studio)

### Prerequisites

- Windows
- Visual Studio 2022 with C++ workload
- SFML 2.6.x installed locally

### Setup

1. Open `DSProj.sln` in Visual Studio.
2. Ensure SFML include/lib paths are set in project properties for every configuration you plan to use (Debug/Release and x64/x86 as needed). The current project explicitly includes SFML path settings for x64 Debug.
3. Build and run the `DSProj` target.

## Important Note About Asset Paths

The current source uses several **hardcoded absolute Windows paths** (for textures/fonts), for example:
- `C:/Users/<username>/Desktop/...`
- `C:/Users/<username>/OneDrive/Desktop/...`

To run the game on another machine, update those paths in `main.cpp` to local paths (or convert them to relative project paths).

## UML Documentation

`uml_diagrams.html` contains multiple UML diagrams (use case, class, sequence, activity, etc.) for the project design.

## Screenshots (Placeholders)

> Add your own images in these sections.

### Main Gameplay

[Insert screenshot here]

### Tower Upgrade UI

[Insert screenshot here]

### Win / Game Over Screen

[Insert screenshot here]

## Future Improvements

- Move all assets to a dedicated `assets/` folder and use relative paths
- Split `main.cpp` into headers/source modules
- Add save/load, more maps, and more tower/enemy classes
- Add cross-platform CMake support
