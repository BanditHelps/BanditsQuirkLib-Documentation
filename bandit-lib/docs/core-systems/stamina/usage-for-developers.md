---
sidebar_position: 1
---

# Adding Stamina to Addonpacks

One of the goals of the YHA Library is to unify abilities and powers from any addon together. As part of this, the YHA Library comes packaged with a global stamina system that anyone can access. Any ability registered with Palladium will automatically be granted properties that allow addon pack developers to tie into the stamina system with ease.

The following properties have been added automatically to **every** ability. See the example below for usage instructions.
| Property      | Description | Default Value | Data Type|
| ----------- | ----------- | ----------- | ----------- |
| initial_stamina      | This value determines how much stamina will be used when the ability is first activated (first-tick). Useful for one time activations, or instant stamina decreases. (Can be used at the same time as stamina_interval_cost)      |    0         | Integer           |
| stamina_interval   | If set to a non-zero value, this property will control the rate in ticks that the stamina is updated while the ability is active. For example, if this is set to 20, the stamina will go down after 1 second of being used. **The "stamina_interval_cost" property must also be defined, or else this does nothing!**       |    0         |   Integer          |
| stamina_interval_cost   | Works in tandem with **stamina_interval**. Defines how much the stamia will go down when the defined interval is reached.        |    0         |   Integer          |

## Examples
### One-time Stamina Use
Uses 20 stamina when a button is pressed.
```json
"use_20_stamina": {
    "type": "palladium:dummy",
    "properties": {
        "title": "Waste Stamina",
        "icon": "minecraft:feather",
        "hidden_in_bar": false,
        "initial_stamina": 20
    },
    "state": {
        "enabling": {
            "type": "palladium:key_bind",
            "behaviour": "action",
            "cooldown": 20
        }
    }
}
```

### Continuous Stamina Usage
Uses 15 stamina every 20 ticks (1 second) while the ability is being held.
```json
"use_stamina_prolonged": {
    "type": "palladium:aim",
    "properties": {
        "title": "Waste Stamina, but constantly",
        "icon": "minecraft:feather",
        "hidden_in_bar": false,
        "stamina_interval": 20,
        "stamina_interval_cost": 15
    },
    "state": {
        "enabling": {
            "type": "palladium:key_bind",
            "behaviour": "held",
            "cooldown": 200
        }
    }
}
```