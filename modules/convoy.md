---
title: Convoy
---

# Convoy

Class: `SFA_Module_Convoy`

Function: `SFA_fnc_moduleConvoy`

[Back to Modules](../)

## What It Is

Convoy creates a moving vehicle group with crews, escorts, route behavior, and optional reinforcement response. It is built for ambushes, escorts, patrol routes, supply runs, prisoner transports, and enemy reaction forces.

Use it when the mission needs a convoy system without hand-scripting every vehicle, waypoint, escort, and reinforcement wave.

## How It Works

The module creates the configured number of convoy vehicles, fills them with crew and escort units, then assigns route behavior. The route can aim toward an end marker or use fallback distance and bearing if no marker route is available.

If reinforcement behavior is enabled, the convoy can send additional units or vehicles after it is attacked. Route markers can be created for debugging or for mission-maker visibility.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| End Marker Name | Marker name used as the convoy destination. This is the cleanest way to point the convoy at a specific endpoint. |
| Fallback Distance | Distance used to generate a fallback destination if no end marker is available. |
| Fallback Bearing | Direction used with fallback distance to choose a fallback route. |
| Convoy Side | Side used by the convoy units. This controls allegiance and default hostility behavior. |
| Convoy Vehicle Classes | Vehicle classnames used by the convoy. Use valid StarForge vehicle classnames for consistent visuals. |
| Vehicle Count | Number of convoy vehicles to spawn. Larger convoys are more cinematic but harder for AI to drive. |
| Crew and Escort Classes | Unit classnames used for vehicle crew and escort infantry. |
| Escorts Per Vehicle | Number of escort units assigned per convoy vehicle. |
| Route Mode | Controls how the convoy route is generated or interpreted. |
| Route Waypoint Spacing | Distance between generated route waypoints. Shorter spacing can help with turns but creates more AI waypoint work. |
| Route Behaviour | AI behavior mode for convoy movement. |
| Route Speed | AI speed mode for convoy movement. |
| Waypoint Completion Radius | Distance from a waypoint before it is considered reached. |
| Send Reinforcements When Hit | Enables reinforcement response after the convoy is attacked. |
| Reinforcement Waves | Number of reinforcement waves available. |
| Reinforcement Groups | Number of infantry groups per wave. |
| Reinforcement Group Size | Unit count inside each reinforcement group. |
| Reinforcement Vehicle Classes | Vehicle classnames used by reinforcing vehicles. |
| Reinforcement Vehicles | Number of vehicles per reinforcement wave. |
| Reinforcement Delay | Time before a reinforcement wave arrives. |
| Reinforcement Cooldown | Minimum time between waves. |
| Reinforcement Spawn Distance | Distance from the convoy where reinforcements spawn. |
| Create Route Markers | Creates markers for generated route/debug visibility. |

## Mission-Maker Notes

- Test the route on the actual terrain. Arma driving is highly map-dependent.
- Keep vehicle count low until the route works reliably.
- For ambushes, make sure the convoy has enough spacing that one disabled vehicle does not trap every vehicle behind it.
- Use route markers while building, then disable them for the live mission if players should not see the path.

## Testing

Verify driving, formation, waypoint completion, reaction to contact, reinforcement timing, cleanup, and server FPS. Dedicated server testing matters more for this module than local editor preview.
