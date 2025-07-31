# **WarGGus**  [WIP]
# Technical Specification

## 1. Introduction
### 1.1 General Description
**WarGGus** is a mod for the [Zug-Zug](https://github.com/ipochto/zug-zug) project, consisting of a set of scripts that describe game objects and implement game logic. To maintain the visual style of Warcraft II, original game assets are used; where needed, new graphics are generated based on those assets - for example, for tilesets.

The **GG** in the name refers to the commonly used expression in the online RTS world ("GG" - good game), emphasizing the project's multiplayer focus.

The project is not a fork of [Wargus](https://github.com/wargus/wargus), but leverages its work wherever appropriate.

### 1.2 Project Goal
To create a multiplayer-oriented classic 2D RTS game in the Warcraft II setting, with a focus on improved balance, new gameplay mechanics, and expanded variability for deeper and more engaging online matches.

### 1.3 Rationale for Development
- A fully-featured solution is needed for modding the original game and providing tools to support its competitive potential, which remains in demand among an still active community.
- The most comprehensive alternative implementation of Warcraft II - the [Wargus](https://github.com/wargus/wargus) + [Stratagus](https://github.com/wargus/stratagus) combination - suffers from stability issues and does not fully support the desired functionality. Its architectural decisions and a significant amount of legacy code make further engine development difficult.
- Gaining development experience.
- Fun, at least.


## 2. Brief Description of Features
* Map Elevation
    - Mechanics providing advantages to units on higher ground
    - Generator for missing tiles in original tilesets
* Line of Sight Limitations
    - Blocked by highgrounds
    - Optionally: by walls, trees, and rocks
    - Some units can partially or fully ignore visibility blocking. For example, towers may see one level higher, and flying units may have unrestricted vision
* Unit Placement and Pathfinding
    - Advanced pathfinding with elements of steering and push behavior
    - Consideration of unit size, weight, and inertia for push behavior
    - Units may be larger than one tile and partially overlap neighboring tiles
    - Collision disabled for workers while gathering resources
    - Air unit stacking
* Improved Local AI (StarCraft-style)
* Global AI with adjustable difficulty levels
* Support for Composite Units
* Transportation
    - Mechanisms for disembarking from sea and air (air transport/magic)
    - Individual transport for large units (e.g., via sling/cargo system)
    - Ability to attack from transports, including while moving
* Fine-Tuned Balance Adjustments with Auto-Correction of Animations:
    - Movement speed
    - Attack speed
    - Cooldowns
* Abilities (spells/skills)
    - Splash attacks, including ones limited to specific segments
    - Knockback attacks
    - Projectile attacks (arc or direct)
    - Charge abilities
    - Fel (with skin color changes)
* Autocast
* Changing Unit Sizes
* Units from Warcraft I (remastered adaptation), possibly as a mod