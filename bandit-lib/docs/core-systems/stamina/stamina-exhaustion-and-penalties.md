---
title: Stamina Exhaustion and Penalties
description: Full breakdown of exhaustion tiers, regen behavior, and all combat/mobility penalties.
sidebar_position: 2
---

# Stamina Exhaustion and Penalties

Exhaustion is the system that makes overusing powers dangerous.  
As your stamina drops below `0`, you move through higher exhaustion tiers with stronger penalties.

## Exhaustion Tiers

| Tier | Stamina Range | Practical Meaning |
| --- | --- | --- |
| 0 | `0` and above | Normal state, no exhaustion penalties |
| 1 | `-10` to `-1` | Light exhaustion |
| 2 | `-35` to `-11` | Moderate exhaustion, damage starts |
| 3 | `-60` to `-36` | Heavy exhaustion, severe penalties |
| 4 | `-61` and lower | Critical exhaustion, lethal risk |

## Regeneration by Tier

Each tier affects both **how long regen waits** and **how quickly stamina comes back**.

| Tier | Regen Delay After Spending | Regen Rate |
| --- | --- | --- |
| 0 | 3 seconds | 1 stamina per second |
| 1 | 6 seconds | 50% chance each second |
| 2 | 8 seconds | 30% chance each second |
| 3 | 9 seconds | 20% chance each second |
| 4 | 10 seconds | 10% chance each second |

Higher tiers recover dramatically slower, so avoiding deep exhaustion is usually more efficient than trying to recover from it.

## Attribute Penalties by Tier

Penalties scale by exhaustion tier and apply automatically.

| Tier | Move Speed | Attack Damage | Attack Speed | Block Break Speed | Jump Strength |
| --- | --- | --- | --- | --- | --- |
| 0 | 0% | 0% | 0% | 0% | 0% |
| 1 | -15% | -25% | -25% | -25% | 0% |
| 2 | -25% | -50% | -50% | -50% | 0% |
| 3 | -35% | -75% | -75% | -75% | -50% |
| 4 | -45% | -100% | -100% | -100% | -100% |

## Exhaustion Damage

If you continue spending stamina while exhausted, you can take direct damage:

- Tier 2 overexertion: `3` damage
- Tier 3 overexertion: `6` damage
- Critical overexertion state can become fatal if you keep forcing stamina use
