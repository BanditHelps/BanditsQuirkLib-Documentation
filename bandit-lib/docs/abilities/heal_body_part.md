---
sidebar_position: 4
---

# HealBodyPart

**Ability Type |** `yha:heal_body_part`

The Heal Body Part ability allows developers to recover health to one or more body parts. Similar to the [DamageBodyPart](./damage_body_part.md) Ability, this ability runs **every tick that it is enabled**.


## Config Values
| Property      | Description | Default Value | Data Type|
| ----------- | ----------- | ----------- | ----------- |
| heal_amount      | This value is how much healing to apply. The value must be **non-negative**, otherwise this ability will do nothing.       |    2.0         | [Value]           |
| parts   | This property accepts an array of body parts to apply the damage to. If more than one part is specified, all parts are damaged equally. <br></br> **Expects: "head" \| "chest" \| "left_arm" \| "right_arm" \| "left_hand" \| "right_hand" \| "left_leg" \| "right_leg" \| "left_foot" \| "right_foot" \| "main_arm" \| "off_arm"**       |    "chest"         |   String[]          |

## Examples

### Single-Part Healing

```json
"mend_arm": {
    "type": "yha:heal_body_part",
    "damage": 50.0,
    "parts": [
        "main_hand"
    ],
    "properties": {
        "title": "Mend Hand",
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

### Multi-Part Healing
```json
"full_heal": {
    "type": "yha:heal_body_part",
    "damage": 100.0,
    "parts": [
        "chest",
        "head",
        "main_arm",
        "off_arm",
        "right_leg",
        "left_leg",
    ],
    "properties": {
        "title": "Full Heal",
        "icon": "minecraft:netherite_chestplate",
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