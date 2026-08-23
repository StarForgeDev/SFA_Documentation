---
title: Convoy and Occupation
---

# Convoy and Occupation Modules

These modules create larger AI-driven mission systems. They should be tested carefully because they can spawn many units, vehicles, and reinforcement groups.

## Convoy

Class: `SFA_Module_Convoy`

Function: `SFA_fnc_moduleConvoy`

The Convoy module spawns a vehicle convoy and sends it toward a destination marker or fallback route.

### Key Convoy Settings

| Setting | Property |
| --- | --- |
| End Marker Name | `SFA_Convoy_EndMarker` |
| Fallback Distance | `SFA_Convoy_FallbackDistance` |
| Fallback Bearing | `SFA_Convoy_FallbackBearing` |
| Convoy Side | `SFA_Convoy_Side` |
| Convoy Vehicle Classes | `SFA_Convoy_VehicleClasses` |
| Vehicle Count | `SFA_Convoy_VehicleCount` |
| Crew and Escort Classes | `SFA_Convoy_UnitClasses` |
| Escorts Per Vehicle | `SFA_Convoy_EscortsPerVehicle` |
| Route Mode | `SFA_Convoy_RouteMode` |
| Route Waypoint Spacing | `SFA_Convoy_RouteSpacing` |
| Route Behaviour | `SFA_Convoy_Behaviour` |
| Route Speed | `SFA_Convoy_Speed` |
| Waypoint Completion Radius | `SFA_Convoy_CompletionRadius` |
| Send Reinforcements When Hit | `SFA_Convoy_EnableReinforcements` |
| Reinforcement Waves | `SFA_Convoy_ReinforcementWaves` |
| Create Route Markers | `SFA_Convoy_CreateMarkers` |

### Convoy Tips

- Use known-good vehicle classnames first.
- Keep vehicle counts low until route behavior is tested.
- For road routes, test on the actual map because AI driving behavior depends heavily on terrain and road network data.

## Occupation Zone

Class: `SFA_Module_Occupation`

Function: `SFA_fnc_moduleOccupation`

The Occupation Zone module populates an area with patrols, garrisons, vehicles, static weapons, checkpoints, and reinforcements.

### Key Occupation Settings

| Setting | Property |
| --- | --- |
| Zone Radius | `SFA_Occupation_Radius` |
| Occupying Side | `SFA_Occupation_Side` |
| Infantry Classes | `SFA_Occupation_InfantryClasses` |
| Patrol Groups | `SFA_Occupation_PatrolGroups` |
| Patrol Size | `SFA_Occupation_PatrolSize` |
| Garrison Units | `SFA_Occupation_GarrisonUnits` |
| Vehicle Classes | `SFA_Occupation_VehicleClasses` |
| Vehicles | `SFA_Occupation_Vehicles` |
| Static Weapon Classes | `SFA_Occupation_StaticClasses` |
| Static Weapons | `SFA_Occupation_Statics` |
| Checkpoints | `SFA_Occupation_Checkpoints` |
| Checkpoint Props | `SFA_Occupation_CheckpointProps` |
| Enable Reinforcements | `SFA_Occupation_Reinforcements` |
| Reinforcement Aircraft | `SFA_Occupation_ReinforcementAir` |
| Create Zone Marker | `SFA_Occupation_CreateMarker` |

### Occupation Tips

- Start with infantry only, then add vehicles and static weapons.
- Keep reinforcement waves low during testing.
- Test server FPS impact before using multiple occupation zones.

## Test Status

Both modules need live Eden and multiplayer validation for spawn ownership, route reliability, cleanup, and performance.
