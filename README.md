[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity

## Group Name
**Makabaka Studio**  
**Members**: Gaofeng Liu, Hankun Liu, Zhengyan Lu

---

## Game World Description

### Objects in the Game World:
- **UI**
  - Seeds Planted Number
  - Seeds Remaining Number

- **Player**
  - Movement: `WASD` to move

- **Seed**
  - Planting: `Space` to plant seeds

---

## Object Attributes and Actions

### Player
- **Attributes**:
  - Bunny sprite
- **Actions**:
  - Move with `WASD`
  - Plant seeds with `Space`
    - **Effect**: 
      - Increases the number of seeds planted.
      - Decreases the number of seeds remaining.
      - Updates these numbers in the UI.

### Plant
- **Attributes**:
  - Plant sprite

### Seed Planted UI
- **Attributes**:
  - Text field
- **Actions**:
  - The count increases when the player plants a seed.

### Seed Remaining UI
- **Attributes**:
  - Text field
- **Actions**:
  - The count decreases when the player plants a seed.

---

## Object Interactions
- **Player**:
  - Plants seeds, which instantiate plants at the player's position when the `Space` key is pressed.
  - Updates the UI to reflect changes in the number of seeds planted and seeds remaining.
- **UI**:
  - Displays real-time feedback based on the player's actions.



## Devlog
Prompt: Include the HW1 break-down exercise you wrote during the Week 1 - Lecture 2 (Jan 9) in-class activity (above). If you did not attend and perform this activity, review the lecture slides and write your own plan for how you believe HW1 should be built. If your initially proposed plan turned out significantly different than the activity answers given by Prof Reid, you may want to note what was different. Then, write about how the plan you wrote in the break-down connects to the code you wrote. Cite specific class names and method names in the code and GameObjects in your Unity Scene.


# Devlog

---

## Game World in Objects  

### Player (Bunny)  
- **Attributes**:
  - Bunny Sprite for character visuals.  
  - Movement speed (`_speed`).  
  - Initial seed count (`_numSeeds`).
- **Actions**:
  - Move using `WASD` keys.  
  - Plant seeds by pressing the `Space` key, which:
    - Instantiates a plant at the bunny's current position.  
    - Decreases the number of seeds remaining.  
    - Updates the seeds planted count on the UI.

### Plant  
- **Attributes**:
  - Visual representation via plant prefab.  
- **Actions**:
  - Appears when a seed is planted.

### Seed Planted UI  
- **Attributes**:
  - Displays the number of seeds planted.  
- **Actions**:
  - Increments whenever the player plants a seed.  

### Seed Remaining UI  
- **Attributes**:
  - Displays the number of seeds left.  
- **Actions**:
  - Decrements whenever the player plants a seed.  

---

## Core Mechanics  

### Movement  
- The bunny moves smoothly in 2D space using the `WASD` keys.  
- Provides players with tactile control over their character's position.  

### Planting Seeds  
- Players can plant seeds by pressing the `Space` key.  
- A seed transforms into a plant at the bunny's position, reducing the remaining seeds and increasing the planted seeds count.  
- Both changes are reflected in the UI.  

---

## Code Implementation

### Player Controls and Actions (`Player.cs`)  

- **Movement**:  
  - Implemented using `Input.GetKey()` for real-time responsiveness.  
  - The bunny moves in the specified direction based on key presses, with speed scaled by `Time.deltaTime`.  
- **Planting Seeds**:  
  - Checks if the player has seeds remaining before instantiating a plant prefab.  
  - Adjust the `_numSeedsLeft` and `_numSeedsPlanted` counters.  
  - Calls `UpdateSeeds()` on the UI component to reflect changes.  

### User Interface Updates (`PlantCountUI.cs`)  
- Automatically update the text to show how many seeds have been planted and how many are left.  
- Ensures real-time feedback for player actions, maintaining clarity.  

---

## Inter-object Interactions  

- **Player** interacts with the **PlantCountUI** to update the on-screen seed counters.  
  - Every time the player plants a seed, the UI updates to show the new numbers, making sure the gameplay and what the player sees match perfectly.  
- **Plant prefab** is spawned right where the player is standing, showing the planted seed as a plant.



## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
