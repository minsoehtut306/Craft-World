# Craft World – Unreal Engine 5 Game

**Craft World** is a third-person puzzle shooter prototype built in **Unreal Engine 5**.  
The player progresses through a series of puzzle rooms before entering an arena and
surviving against waves of enemies under a global countdown timer.

This project was created as part of my Bachelor of Computer Science and used as a
sandbox to learn **UE5 Blueprints, game architecture, AI behaviour, and HUD design**.

---

## Gameplay Overview

The player has **2 minutes** to reach the end of the level.

1. **Room 1 – Basic Door Button**  
   Press a visible button to open the door and proceed.

2. **Room 2 – Hidden Button**  
   Search the room to find and press a concealed button that unlocks the door.

3. **Room 3 – Light Puzzle**  
   Activate four light switches. When all lights are on, the door will open.

4. **Room 4 – Rock Placement Puzzle**  
   Collect rocks, return them to the correct pedestals, trigger an animation
   sequence, and open the next door.

5. **Room 5 – Arena**  
   A combat arena where the player must fight AI enemies until the timer runs out.
   Enemies spawn in waves from multiple points.

---

## Core Systems & Mechanics

### Puzzle & Level Logic
- **Button–Door system**  
  - Buttons and doors share IDs; pressing a button finds the matching door and triggers its animation.  
  - Optional camera cut to highlight the door when it opens.
- **Light door puzzle**  
  - Trigger boxes detect interaction.  
  - When all four lights are active, the door is flagged as unlocked.
- **Rock puzzle**  
  - Collectable rock items.  
  - When all rocks are placed on the correct spots, a sequence plays:
    rocks move into position, SFX is played, and the door opens.
- **Arena intro**  
  - Opening the arena door triggers a simple cutscene before combat begins.

### Player Systems
- **Interaction system**  
  - `E` to interact with any actor that implements a shared “Interact” interface
    (buttons, rocks, pickups, etc.).
- **Health, damage, and death**  
  - Player takes damage from AI attacks and debug key presses.  
  - A **safe zone** prevents damage inside protected areas.  
  - On zero health, the player dies and the game ends.
- **Healing system**  
  - Heal action checks maximum health and plays a sound on successful heal.
- **Speed & stamina**  
  - Sprinting increases movement speed and drains stamina; stamina regenerates
    when the player stops running.
- **Shooting & reloading**  
  - Left mouse: fire bullet if not reloading and there is ammo.  
  - Right mouse: aim (narrowed FOV / zoom).  
  - Reload logic recalculates ammo in magazine vs. reserve and supports
    “infinite ammo” for testing.
- **HUD widgets**  
  - Health and stamina bars  
  - Ammo (magazine + total)  
  - Kill count  
  - Global countdown timer  
  - Game-over screen when time expires or the player dies.

### Combat & AI
- **Enemy behaviour**
  - Enemies chase the player when the game starts or when they enter the arena.  
  - When hit, enemies play a hit animation, briefly pause, and then resume chasing.  
  - On zero health, enemies play a death animation, play a sound, remain on the
    ground for a short period, then are removed.
- **Enemy damage**
  - When the player overlaps an enemy damage trigger, health is reduced and SFX plays.
- **Enemy spawner**
  - Loops through configured spawn points, spawning a set number of enemies at
    each location with individually defined delays.
- **Pickups**
  - Collectable items that increase enemy walk speed each time one is collected,
    dynamically increasing difficulty.

---

## Animation, Audio & UI

- **Animations**  
  - Based on public educational resources (e.g., Matt Aspland), blended and adjusted
    for aiming, movement, and death states.
- **Sound**  
  - All SFX sourced from **Freesound**, using assets that allow copying,
    modification, and redistribution (including commercial use).
- **Widgets**
  - **Ammo widget** – magazine + total ammo  
  - **Kill counter** – total enemies defeated  
  - **Timer widget** – global countdown until game ends  
  - **Game over widget** – displays when time expires  
  - **Health & stamina widgets** – keep the player informed at all times

---

## Controls

- `WASD` – Move  
- `Shift` – Sprint  
- `Space` – Jump  
- `E` – Interact (buttons, rocks, pickups)  
- `Left Mouse` – Shoot  
- `Right Mouse` – Aim  
- `R` – Reload  
- `V` – Toggle first/third-person camera  
- `1` – Apply damage to self (debug)  
- `2` – Heal (debug)

---

## Project Setup

1. Install **Unreal Engine 5**.  
2. Clone or download this repository.  
3. Open `P2CraftWorld.uproject` in UE5.  
4. Press **Play** in the editor to start the game.

---

## Learning Outcomes

Through **Craft World** I gained experience in:

- Structuring gameplay logic with **Blueprints** (puzzles, AI, HUD, timers).  
- Designing multi-room game flow with clear objectives and feedback.  
- Implementing and debugging core shooter mechanics (ammo, reloading, aiming).  
- Building AI behaviours and spawn systems that scale difficulty.  
- Balancing scope, time, and polish in a solo UE5 project.

Planned improvements include smoother animation blending, more polished combat
feedback, and visual/environmental refinement.

---

## Notes & Academic Integrity

This project was created as part of my **Bachelor of Computer Science** at the
**University of Waikato** and is published here for **portfolio and learning
purposes only**.

- All gameplay logic and integration code is my own work.  
- If required, I am happy to adjust or remove this repository on request.
