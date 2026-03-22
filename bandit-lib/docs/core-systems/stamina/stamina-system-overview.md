---
title: Stamina System Overview
description: Player guide to how stamina works, how it is spent, and how to stay effective in combat and movement.
sidebar_position: 1
---

# Stamina System Overview

Stamina is your physical energy pool. Most active powers consume stamina, and overusing your abilities can push you into exhaustion.  
Managing stamina well is one of the biggest differences between short bursts of power and consistent performance in long fights.

## Core Rules

- You have two values: **Current Stamina** and **Max Stamina**.
- Abilities reduce current stamina when activated and/or while held.
- Stamina can go below zero, which increases your exhaustion tier.
- The lower your stamina goes, the harsher your penalties become.
- If you keep forcing stamina use while deeply exhausted, you can take heavy damage or die.

## Starting Stamina

When a player first logs into a world, max stamina is randomized in this range:

- **Minimum start:** `80`
- **Maximum start:** `120`

## How Stamina Is Spent

Abilities can consume stamina in two common ways:

- **Activation cost:** a one-time cost when the ability turns on.
- **Interval cost:** repeating cost every set interval while the ability stays active.

This means some powers are burst-heavy, while others drain stamina over time.

## Natural Regeneration

Stamina regeneration is not instant:

- After spending stamina, a short **regen delay** begins.
- Once the delay ends, stamina regenerates over time.
- Higher exhaustion tiers have longer delays and slower regeneration.

Full regen details are covered in the exhaustion page.

## Death and Respawn Behavior

To help balance stamina training and prevent easy stamina obtainment, certain values will be reset during a respawn. When a player dies, the following occurs:

- Current stamina is restored to full.
- Exhaustion and regen delay are cleared.
- Progress towards additional max stamina is reset.
- Progress towards the next upgrade point is reset.