---
title: Zero-G Area
---

# Zero-G Area

Class: `SFA_Module_ZeroG`

Function: `SFA_fnc_moduleZeroG`

The Zero-G Area module creates a configurable movement zone for players and, optionally, AI. It is intended for spaceships, stations, damaged interiors, vacuum sections, and special mission set pieces.

## Basic Setup

1. Place `Zero-G Area` from the `SFA Modules` Eden category.
2. Position the module at the center of the affected area.
3. Set the zone size in Eden using the module area controls.
4. Tune thrust, speed, drag, floor clamping, and AI settings.
5. Test in the same environment the mission will use: singleplayer, hosted multiplayer, or dedicated server.

## Key Settings

| Setting | Property | Use |
| --- | --- | --- |
| Enabled | `SFA_ZeroG_Enabled` | Turns the module behavior on or off. |
| Thrust | `SFA_ZeroG_Thrust` | Base movement force while floating. |
| Boost Thrust | `SFA_ZeroG_BoostThrust` | Movement force while boosting. |
| Maximum Speed | `SFA_ZeroG_MaxSpeed` | Normal speed cap. |
| Boost Maximum Speed | `SFA_ZeroG_BoostMaxSpeed` | Boost speed cap. |
| Drift Drag | `SFA_ZeroG_Drag` | Slows uncontrolled drift. |
| Q/E Roll Speed | `SFA_ZeroG_RollSpeed` | Controls roll speed. |
| Magnetic Floor Clamping | `SFA_ZeroG_SurfaceClamp` | Allows walking on valid floor surfaces when close enough. |
| Floor Clamp Distance | `SFA_ZeroG_ClampDistance` | Maximum distance to a floor surface before clamp applies. |
| Maximum Floor Slope | `SFA_ZeroG_NativeWalkAngle` | Maximum surface slope treated as floor-walkable. |
| Floor Jump Release Speed | `SFA_ZeroG_ClampJumpSpeed` | Jump speed when leaving a clamped floor. |
| Preserve Entry Momentum | `SFA_ZeroG_KeepEntryMomentum` | Keeps existing velocity when entering the zone. |
| Weapon Recoil Push | `SFA_ZeroG_WeaponRecoil` | Adds recoil movement while floating. |
| Affect AI | `SFA_ZeroG_AffectAI` | Enables AI handling inside the zone. |
| AI Arrival Radius | `SFA_ZeroG_AIArrivalRadius` | How close AI needs to get to a target destination. |

## Behavior Notes

- Current source notes indicate floor-only magnetic clamping. Do not document wall or ceiling walking as supported unless it is intentionally re-added and tested.
- Player movement should be treated as client-facing behavior. Verify hosted multiplayer, dedicated server, JIP, and headless-client behavior separately.
- AI behavior should be tested with several unit counts before using it in a live operation.

## Example Mission Use

Use this module inside a derelict ship section:

- Set `Magnetic Floor Clamping` on.
- Keep `Maximum Floor Slope` conservative so walls and ceilings are rejected.
- Use lower drift drag for open hangars and higher drag for cramped interiors.
- Disable `Affect AI` unless the encounter specifically needs AI in the zone.

## Test Status

Source-level documentation exists. Runtime behavior still needs mission-specific validation after packing the addon.
