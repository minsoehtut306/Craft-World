# Craft World – Unreal Engine 5 Game Project

**Craft World** is a third-person puzzle and shooter game built with **Unreal Engine 5**.  
The goal is to solve puzzles across multiple rooms and survive until the timer runs out.  
This project served as a hands-on learning experience in puzzle mechanics, shooting systems, AI, and UE5 Blueprints.

---

## Gameplay Overview

The player has **2 minutes** to complete the game by progressing through puzzle rooms and defeating enemies.

- **Room 1** – Press a button to open the door.  
- **Room 2** – Find the hidden button to open the door.  
- **Room 3** – Activate four lights to unlock the next door.  
- **Room 4** – Collect and place rocks in the correct locations to open the door.  
- **Room 5 (Arena)** – Defeat waves of enemies until the timer runs out.  

---

## Core Mechanics

- **Puzzle Logic**  
  - Button and door system with linked IDs.  
  - Light activation puzzle.  
  - Rock placement puzzle with animations and sound effects.  
  - Arena with cutscene and timer system.  

- **Player Systems**  
  - Health, stamina, and death system.  
  - Interact system (buttons, collectables).  
  - Aiming, shooting, and reloading with ammo system.  
  - Healing system and safe zones.  
  - HUD widgets for health, stamina, ammo, kill count, and timer.  

- **Combat & AI**  
  - Enemies chase the player and deal damage.  
  - Enemy health, damage, and death animations.  
  - Enemy spawner with configurable units and delays.  
  - Collectables that increase enemy speed.  

- **Animation & Sound**  
  - Basic animations (public resources, educational use).  
  - Free sound effects (Freesound, free for modification/distribution).  
  - Muzzle flash and shooting effects.  

---

## Development Notes

- **Software:** Unreal Engine 5  
- **Time Investment:** ~60 hours for modelling + ~8 hours for documentation.  
- **Estimated Cost:** ~$1000 development value.  
- **Project File:** `P2CraftWorld.uproject`  

---

## Learning Outcomes

Through this project, the following skills were developed:

- Blueprint scripting for puzzles, shooting, AI, and HUD systems.  
- Designing logical game flow with multiple rooms.  
- Creating and debugging interactive mechanics.  
- Balancing gameplay with timers, spawns, and health systems.  
- Integrating animations, sounds, and widgets into a cohesive experience.  

---

## Achievements & Future Work

- Completed puzzle flow (Rooms 1–4).  
- Implemented basic third-person shooting system.  
- AI enemy logic and spawner system.  

**To improve further:**  
- Refine animation blending and transitions.  
- Polish combat mechanics for smoother gameplay.  
- Add more visual/texture variety for immersive experience.  

---

## How to Open

1. Open `P2CraftWorld.uproject` in **Unreal Engine 5**.  
2. Press **Play** to test the game.  
3. Use the following key bindings:  
   - `E` → Interact  
   - `V` → Toggle First/Third Person  
   - `Left Mouse` → Shoot  
   - `Right Mouse` → Aim  
   - `R` → Reload  
   - `1` → Apply damage to self (debug)  
   - `2` → Heal  
   - Standard movement keys (`WASD`, Shift to run)  

---

## Conclusion

**Craft World** demonstrates puzzle integration with third-person shooter mechanics in UE5.  
It highlights the process of combining Blueprints, AI, animations, and logic into an engaging prototype game.  
While additional polish is needed, the project was a valuable step in understanding game design and development. 
 
---

### Note

This project was completed as part of the Bachelor of Computer Science degree at the University of Waikato.  
It is published here solely for educational and portfolio purposes, to showcase my skills in software development.  

All code presented is my own work. Course-specific materials such as assignment descriptions or test data are not included to respect university policies.  

## Academic Integrity
Portfolio-only; not intended for reuse in coursework. Removal on request.
