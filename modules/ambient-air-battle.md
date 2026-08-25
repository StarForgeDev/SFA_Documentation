---
title: Ambient Air Battle
---

# Ambient Air Battle

Class: `SFA_Module_AmbientAirBattle`

Function: `SFA_fnc_moduleAmbientAirBattle`

[Back to Modules](../)

## What It Is

Ambient Air Battle is a cinematic background-combat module. It creates the impression of a larger fight happening above or around the playable area by spawning aircraft or starfighters for two opposing sides.

Use it when the mission needs movement, sound, and visual action in the sky without requiring the players to personally fight every aircraft. It works best as atmosphere for an assault, evacuation, orbital battle, fleet attack, invasion, or base defense.

It is not meant to be the main objective controller for an air-superiority mission. If players must destroy specific aircraft to complete an objective, place and script those objective aircraft separately.

## How It Works

The module uses its position as the center of the air battle. When active, it spawns a configured number of ships per side, places them within the spawn radius, and lets them travel or fight inside the configured travel radius and height band.

The mission maker controls the battle volume with radius, altitude, and height spread. The module controls the look of the battle by using the BLUFOR and REDFOR model/class settings. The duration settings decide whether the effect ends after a timed scene or stays active as long-term ambience.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Duration | Sets how long the air battle runs. Use a short duration for intros or set pieces; use a longer duration for missions where the battle should remain visible while players move. |
| Unlimited Duration | Overrides the normal timer and keeps the air battle running. Use this for constant background warfare, but test performance before using it in long operations. |
| Ships Per Side | Controls how many aircraft each side receives. Higher values look more dramatic but cost more performance and can make the sky visually noisy. |
| Spawn Radius | Controls how far from the module aircraft can initially appear. A larger radius spreads the battle out; a smaller radius concentrates the action near the mission area. |
| Travel Radius | Controls how wide the aircraft movement area is after spawning. Use this to keep the battle above a city, battlefield, landing zone, or fleet area. |
| Battle Height | Sets the base altitude for the aircraft. Low values make the fight feel close and dangerous; high values make it background scenery. |
| Height Spread | Adds vertical variation above and below the base battle height. More spread makes the battle less flat and more natural. |
| Ship Speed | Controls aircraft movement speed. Higher speed makes passes more dramatic, but can make aircraft harder to see and may stress AI/pathing behavior. |
| BLUFOR Model | Aircraft or ship classname used for the friendly side. |
| REDFOR Model | Aircraft or ship classname used for the hostile side. |

## Mission-Maker Notes

- Place it away from tight terrain if aircraft are clipping into buildings or mountains.
- Use faction-appropriate ship classnames so the scene matches the mission.
- Keep ship counts conservative until the mission has been tested with all other AI systems active.
- If the air battle is only visual, do not tie main objectives to its spawned units unless you have verified cleanup and ownership behavior.

## Testing

Test this module in the actual terrain and weather used by the mission. Verify spawned aircraft height, visibility, cleanup, performance, and whether clients joining in progress see the intended scene.
