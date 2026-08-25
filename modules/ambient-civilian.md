---
title: Ambient Civilian
---

# Ambient Civilian

Class: `SFA_Module_AmbientCivilian`

Function: `SFA_fnc_moduleAmbientCivilian`

[Back to Modules](../)

## What It Is

Ambient Civilian populates non-combat spaces with civilian pedestrians, traffic, police, and cleanup behavior. It is intended for settlements, ports, markets, city streets, refugee camps, corporate facilities, and underworld hubs.

Use it when a StarForge mission needs an area to feel occupied without hand-placing every civilian and vehicle.

## How It Works

The module monitors the configured area and periodically spawns ambient units according to the enabled systems and class lists. Pedestrians and traffic are separate, and police can be enabled as an additional layer.

The module also uses distance controls so units do not appear directly in front of players and can be cleaned up once they are far away. This is important because civilian systems can become expensive if old units are never removed.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Enable Pedestrians | Turns civilian foot traffic on or off. |
| Enable Traffic | Turns ambient civilian vehicles on or off. |
| Max Pedestrians | Maximum active pedestrian count. Raise this for busy cities; lower it for small outposts or performance. |
| Max Traffic Vehicles | Maximum active traffic vehicle count. Keep this conservative on maps with poor road networks. |
| Enable Police | Adds police/security presence to the ambient system. |
| Max Police | Maximum active police unit count. |
| Max Police Vehicles | Maximum active police vehicle count. |
| Spawn Radius | How far from players or eligible areas ambient units can spawn. |
| Min Player Distance | Minimum safe distance from players before a unit can appear. This prevents visible pop-in. |
| Cleanup Distance | Distance at which ambient units can be removed. Larger values keep ambience longer but cost more performance. |
| Spawn Interval | Time between spawn checks. Short intervals react faster; long intervals are cheaper. |
| Town Bias | Weights spawning toward towns or settlement areas. |
| Civilian Classes | Unit classnames used for pedestrians. |
| Vehicle Classes | Vehicle classnames used for traffic. |
| Police Classes | Unit classnames used for police/security. |
| Police Vehicle Classes | Vehicle classnames used for police/security vehicles. |

## Mission-Maker Notes

- Keep civilians disabled in active firefight zones unless the mission is built around civilian presence.
- Use faction-appropriate civilian and police classes for the planet or city.
- Do not set cleanup distance too low or players may see civilians disappear.
- Do not set spawn distance too low or players may see civilians appear.

## Testing

Verify civilian density, traffic pathing, cleanup, and performance after other AI systems are also active. Traffic behavior depends heavily on the terrain's road data.
