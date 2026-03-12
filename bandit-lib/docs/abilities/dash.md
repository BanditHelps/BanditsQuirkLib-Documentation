---
sidebar_position: 2
---

# Dash

The Dash ability allows the user to quickly move in the direction that they are looking, or in the direction opposite. This is a pretty versatile movement ability, allowing the user to even "leap" in the direction they are looking, or do a simple sprint forward.

An important note about the dash is that it operates differently wether the player is touching the ground or in the air. Each state is modified accordingly to account for friction, ensuring that the dash distance is similar in both situations.  

## Config Values
| Property      | Description | Default Value | Data Type|
| ----------- | ----------- | ----------- | ----------- |
| strength      | This corresponds to the speed and distance the dash will have upon use. The higher the value, the further the dash. Making this value negative will change the direction. **THIS IS NOT THE NUMBER OF BLOCKS THAT THE PLAYER MOVES**.       |    2.0         | [Value]           |
| block_vertical   | This value will determine wether or not the player can dash in a vertical direction direction or not. Setting this to true will allow them to dash into the air, similar to a leap. Keeping it false locks movement to the horizontal axis only.       |    true         |   Boolean          |