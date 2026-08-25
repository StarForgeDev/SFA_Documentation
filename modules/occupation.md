---
title: Occupation Zone
---

# Occupation Zone

Class: `SFA_Module_Occupation`

Function: `SFA_fnc_moduleOccupation`

[Back to Modules](../)

## What It Is

Occupation Zone fills an area with a military presence. It can create patrols, garrisons, vehicles, static weapons, checkpoints, zone markers, and reinforcements.

Use it for enemy-held towns, military checkpoints, FOB defenses, base assaults, occupied settlements, or quick defensive layouts.

## How It Works

The module uses its placed position as the center of the occupied area. It reads the zone radius, chosen side, unit class lists, and spawn counts. Then it creates patrols, garrison units, vehicles, static weapons, and checkpoints according to the enabled settings.

If reinforcements are enabled, the zone can respond after contact with additional infantry, vehicles, or aircraft. The zone marker setting can expose the area visually for setup, debugging, or player-facing objectives.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Zone Radius | Size of the occupied area around the module. |
| Occupying Side | Side that owns the zone. This controls spawned unit allegiance. |
| Infantry Classes | Unit classnames used for patrol and garrison infantry. |
| Patrol Groups | Number of patrol groups spawned in the zone. |
| Patrol Size | Number of units in each patrol group. |
| Garrison Units | Number of defensive units placed as garrison presence. |
| Vehicle Classes | Vehicle classnames available to the occupation system. |
| Vehicles | Number of vehicles placed in the zone. |
| Static Weapon Classes | Turret/static weapon classnames available to the zone. |
| Static Weapons | Number of static weapons placed. |
| Checkpoints | Number of checkpoint positions created. |
| Checkpoint Props | Prop classnames or composition pieces used for checkpoints. |
| Enable Reinforcements | Allows the zone to call reinforcement waves. |
| Reinforcement Waves | Number of reinforcement waves available. |
| Reinforcement Groups | Number of infantry groups in each wave. |
| Reinforcement Group Size | Unit count in each reinforcement group. |
| Reinforcement Vehicle Classes | Vehicle classnames used by ground reinforcements. |
| Reinforcement Vehicles | Number of ground reinforcement vehicles. |
| Reinforcement Air Classes | Aircraft classnames used by air reinforcements. |
| Reinforcement Aircraft | Number of aircraft in a reinforcement wave. |
| Reinforcement Delay | Time before reinforcements arrive after being triggered. |
| Reinforcement Cooldown | Time between reinforcement waves. |
| Reinforcement Spawn Distance | Distance from the zone where reinforcements spawn. |
| Create Zone Marker | Creates a marker for the occupied area. |

## Mission-Maker Notes

- Build in layers: infantry first, then statics, then vehicles, then reinforcements.
- Use checkpoint props carefully on uneven terrain.
- Keep garrison and patrol counts realistic for the area size.
- Avoid placing multiple large occupation zones close together unless you have tested server FPS.

## Testing

Verify spawn placement, patrol movement, garrison behavior, static weapon orientation, checkpoint placement, reinforcement triggers, cleanup, and performance.
