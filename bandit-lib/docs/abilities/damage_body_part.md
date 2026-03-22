---
sidebar_position: 2
---

# Damage Body Part

**Ability Type |** `yha:damage_body_part`

The Damage Body Part ability allows developers to apply damage to one or more body parts. This ability runs **every tick that it is enabled**, so be careful.


## Config Values
| Property      | Description | Default Value | Data Type|
| ----------- | ----------- | ----------- | ----------- |
| damage      | This value is how much damage to apply. The value must be **non-negative**, otherwise this ability will do nothing.       |    2.0         | [Value]           |
| parts   | This property accepts an array of body parts to apply the damage to. If more than one part is specified, all parts are damaged equally. <br></br> **Expects: "head" \| "chest" \| "left_arm" \| "right_arm" \| "left_hand" \| "right_hand" \| "left_leg" \| "right_leg" \| "left_foot" \| "right_foot" \| "main_arm" \| "off_arm"**       |    "chest"         |   String[]          |

## Examples

### Single-Part Damage

```json
"hand_sprain": {
    "type": "yha:damage_body_part",
    "damage": 10.0,
    "parts": [
        "right_hand"
    ],
    "properties": {
        "title": "Hurt Hand",
        "icon": "minecraft:wooden_sword",
        "hidden_in_bar": false
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

### Multi-Part Damage
```json
"whole_body_contusion": {
    "type": "yha:damage_body_part",
    "damage": 5.0,
    "parts": [
        "chest",
        "head",
        "main_arm",
        "off_arm",
        "right_leg",
        "left_leg",
    ],
    "properties": {
        "title": "Full Body Damage",
        "icon": "minecraft:netherite_sword",
        "hidden_in_bar": false
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