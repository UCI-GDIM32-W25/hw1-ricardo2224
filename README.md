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


Write your Devlog here!


## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
