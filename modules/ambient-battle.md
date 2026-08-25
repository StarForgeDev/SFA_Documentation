---
title: Ambient Battle
---

# Ambient Battle

Class: `SFA_Module_AmbientBattle`

Function: `SFA_fnc_moduleAmbientBattle`

[Back to Modules](../)

## What It Is

Ambient Battle creates a configurable ground battle around the module. It can spawn infantry groups and vehicles for BLUFOR, OPFOR, and INDFOR, then make those sides fight in the chosen area.

Use it when you need a battlefield to feel alive: a front line, base assault, city fight, trench battle, patrol clash, or background engagement that supports the main mission.

It is a population and ambience tool. For precise objectives, hand-place the key units or create separate objective logic so the mission does not depend entirely on ambient spawns.

## How It Works

The module reads which sides are enabled, chooses units from the class lists for those sides, creates the requested number of groups, and places them inside the battle radius. If vehicles are enabled, it also creates vehicle presence for the sides. Force Side Hostility can be used to make spawned sides engage even if the mission's side relations are not already configured.

The result is a controlled combat bubble around the module. The main tuning choices are how large the bubble is, how many groups spawn, how large those groups are, which unit classnames are used, and how long the fight lasts.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Battle Radius | Defines the size of the combat area. A larger radius spreads units out; a smaller radius creates a denser firefight. |
| BLUFOR In Battle | Enables friendly-side spawns. Disable it if the scene should be enemy-only or if friendly units are manually placed. |
| REDFOR In Battle | Enables OPFOR spawns. Use this for Sith, Separatist, plague, or other hostile StarForge forces. |
| GREENFOR In Battle | Enables INDFOR spawns. Use this for third-party forces like Mandalorians, Czerka, Hutt Cartel, or Onderon when appropriate. |
| Groups Per Side | Number of infantry groups spawned for each enabled side. This is one of the biggest performance and difficulty controls. |
| Group Size | Number of soldiers in each infantry group. Larger groups are more intense but harder for AI to path in tight spaces. |
| BLUFOR Classes | Unit classnames used for BLUFOR groups. Use StarForge Republic or allied classnames for consistent visuals. |
| REDFOR Classes | Unit classnames used for OPFOR groups. Use Sith, Separatist, plague, or other hostile classnames. |
| GREENFOR Classes | Unit classnames used for INDFOR groups. Use independent faction classnames. |
| Vehicles Per Side | Number of vehicles spawned for each side. Vehicles raise difficulty and performance cost quickly. |
| Force Side Hostility | Forces the spawned sides to treat each other as enemies. Use this when the map or mission has custom side relations. |
| Duration | How long the ambient battle remains active before it should end or clean itself up. |

## Mission-Maker Notes

- Start with infantry only, confirm the fight behaves correctly, then add vehicles.
- Keep the radius large enough that groups do not spawn directly on top of each other.
- Use known-good classnames. Invalid classnames can silently break the scene or create missing-unit behavior.
- Avoid running several large ambient battle modules at the same time unless server FPS has been tested.

## Testing

Test side hostility, spawn density, cleanup, AI movement, and server FPS. If the mission is multiplayer, test on a hosted or dedicated environment instead of relying only on local Eden preview.
