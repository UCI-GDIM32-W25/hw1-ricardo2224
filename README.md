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

# Devlog

## Construction

Based on the in-class activity, I structured HW1 by breaking the game into three main components: the Player, UI elements (Seeds Planted and Seeds Remaining), and Plants. The core mechanics involve player movement and seed planting, with dynamic updates reflected in the UI. This approach ensured a clear focus on integrating game actions and visual feedback.

## Code Part

The initial plan translated into the code implementation as follows:

- **Player Movement and Actions:**  
  In the `Player.cs` script, movement is controlled using `Input.GetKey()` for WASD keys, while planting seeds is triggered by the Space key. Planting seeds decreases `_numSeedsLeft`, increases `_numSeedsPlanted`, and spawns a plant prefab at the player’s position.

- **UI Updates:**  
  The `PlantCountUI.cs` script manages the UI text fields for seeds planted and remaining. The `UpdateSeeds()` method is called each time a seed is planted to ensure real-time updates, providing consistent feedback to the player.

## Challenges and Solutions

The primary challenge was ensuring UI updates occurred in real-time. Initially, the UI text fields failed to refresh immediately after planting seeds. This was resolved by introducing the `UpdateSeeds()` method in the UI script and invoking it whenever seed counts changed. Testing this method step by step confirmed the issue was fixed.

## Key Takeaways

This project taught me to break down game mechanics into manageable components and integrate them effectively using scripts. I gained a deeper understanding of the importance of real-time UI feedback in enhancing player experience. 

## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites

## Prof comments
Thank you for formatting your Devlog neatly and for clearly connecting the break-down activity to the code you wrote. This was most clear in the sections titled 'Construction' and 'Code Part' - to be honest, I don't think the 'challenges and solutions' and 'key takeaways' sections were totally necessary as they don't really address the prompt. Also, you can also remove the prompts from your submitted Devlogs. Good job overall!
