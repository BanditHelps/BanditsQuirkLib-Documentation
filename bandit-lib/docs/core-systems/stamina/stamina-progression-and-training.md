---
title: Stamina Progression and Training
description: How max stamina grows, how upgrade point progress is earned, and how treadmill training fits into progression.
sidebar_position: 3
---

# Stamina Progression and Training

Stamina progression has two parallel tracks:

- **Max stamina growth** (your long-term stamina pool increases over time)
- **Upgrade point progress** (earned by pushing stamina under pressure)

Both reward active stamina use, but they are triggered in different ways.

## 1) Max Stamina Growth

Each player has an internal tracker for the total stamina usage over time.

- Once a player has accumulated **100 stamina usage**, using further stamina triggers a chance to gain max stamina
  - Normal state chance: **5%**
  - Exhausted state chance: **10%**
- On a successful roll, max stamina increases by **1 to 3**.
- After a successful increase, usage progress resets and begins building again.

### Excercising

The 1.21.11 version of Your Hero Academia has begun to add new ways of training player's stamina. One of these ways is via excercise blocks. 

#### Treadmill
While on the treadmill, player's will passively gain **stamina usage** at the cost of their hunger bar, allowing them to increase max stamina without risking exhaustion.

To use a treadmill:
- Right-click a treadmill to start training.
- While active, your player is kept positioned on the treadmill.
- Crouching will exit

## 2) Upgrade Point Progress

Upgrade points are earned by spending stamina while under pressure.

### Conditions to Gain Progress

You only gain upgrade progress if all of these are true:

- You spent positive stamina.
- Your current stamina is at or below **33% of max** after that spend.
- Upgrade progress is not on cooldown.

### Progress Formula

Progress to an upgrade point is calculated by multiplying stamina used by the exhaustion multipliers below:

- Tier 0: `x1.0`
- Tier 1: `x1.2`
- Tier 2: `x1.5`
- Tier 3: `x2.0`
- Tier 4: `x3.0`

When total progress reaches **500**, you gain **1 upgrade point**.

### Important Upgrade Point Rules

- Progress does **not** carry over after earning a point (it resets to 0).
- Progress **resets** on player death.
- There is a cooldown of **60 seconds** after earning an upgrade point, where no progress can be earned.

These rules were designed to help prevent AFK point farming, and spamming high stamina abilities.
