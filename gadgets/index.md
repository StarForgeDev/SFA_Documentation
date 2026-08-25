---
title: Gadgets
---

# StarForge Gadgets

StarForge gadgets are inventory-carried player tools. They are not generic Arma weapons in the normal loadout sense. The gadget system gives players a selected gadget, handles activation, manages cooldown or state, and displays feedback through the StarForge HUD.

## Gadget List

| Gadget | Classname | What it is |
| --- | --- | --- |
| Wrist Rocket | `SFA_WristRocket_Gadget` | A wrist-mounted explosive gadget that fires `SFA_WristRocket_Ammo` through the shared gadget launcher path. |
| Electro Dart | `SFA_ElectroDart_Gadget` | A dart gadget intended for disabling or stunning targets using `SFA_ElectroDart_Ammo`. |
| Concussive Missile | `SFA_ConcussiveMissile_Gadget` | A heavier wrist-fired explosive gadget using `SFA_ConcussiveMissile_Ammo`. |
| Energy Shield | `SFA_EnergyShield_Gadget` | Defensive gadget that projects or manages an energy shield state. |

Shared support classes:

| Classname | Purpose |
| --- | --- |
| `SFA_Gadget_Base` | Base inventory item inherited by the gadget items. |
| `SFA_Gadget_ItemInfo` | Shared item info definition used by gadget gear. |
| `SFA_WristRocket_Launcher` | Hidden/shared launcher path used by wrist-fired gadget projectiles. |

## How Gadgets Work

The gadget system is built around three parts:

1. A carried gadget item, such as `SFA_WristRocket_Gadget`.
2. Support ammo or launcher classes when the gadget needs to fire a projectile.
3. Client-side player logic and HUD display so the player can see selected gadget state and activation feedback.

The important design point is that the gadget item is the player-facing gear. The projectile, ammo, and launcher classes are support classes. Mission makers should normally give the player the gadget item, not manually equip the hidden launcher unless a specific test requires it.

## Wrist Rocket

The Wrist Rocket is an offensive gadget for a quick explosive shot.

How it works:

- The player carries `SFA_WristRocket_Gadget`.
- Activation routes through the gadget system.
- The system uses `SFA_WristRocket_Mag` and `SFA_WristRocket_Ammo` for the projectile behavior.
- It is best used as limited-use ordnance rather than a primary weapon.

Mission-maker notes:

- Give it to units that should have Mandalorian-style wrist ordnance.
- Balance it around cooldowns, ammo availability, or mission restrictions.
- Avoid handing it to every unit unless the mission is designed for heavy explosive spam.

## Electro Dart

The Electro Dart is a control gadget. It is meant for disabling, stunning, or interrupting targets rather than replacing a blaster.

How it works:

- The player carries `SFA_ElectroDart_Gadget`.
- Activation fires or applies the dart payload using `SFA_ElectroDart_Mag` and `SFA_ElectroDart_Ammo`.
- Effects should be checked in live gameplay because hit behavior depends on target, locality, and configured damage/effect handling.

Mission-maker notes:

- Use it for bounty hunter, stealth, capture, interrogation, and non-lethal encounter setups.
- If a target must be captured for an objective, test that the target survives and that the objective logic detects the state correctly.

## Concussive Missile

The Concussive Missile is the heavier explosive wrist gadget.

How it works:

- The player carries `SFA_ConcussiveMissile_Gadget`.
- Activation uses `SFA_ConcussiveMissile_Mag` and `SFA_ConcussiveMissile_Ammo`.
- It should be treated as heavier ordnance than the Wrist Rocket.

Mission-maker notes:

- Use for anti-personnel shock, bunker-breach moments, or special enemy kits.
- Test blast radius and friendly-fire risk before using it in tight interiors.

## Energy Shield

The Energy Shield is a defensive gadget.

How it works:

- The player carries `SFA_EnergyShield_Gadget`.
- Activation changes the player's shield state through the gadget system.
- The HUD should show selected gadget and active/ready feedback so the player understands when the shield is available.

Mission-maker notes:

- Use for special classes, Mandalorian loadouts, bosses, or survival encounters.
- Test the shield in multiplayer before building objectives around it because defensive effects are sensitive to damage handling and locality.

## HUD System

The StarForge HUD is the player-facing status layer for gadgets and related systems. It exists so players do not need to guess which gadget is selected, whether a gadget is ready, or whether a system is active.

How the HUD works:

- It displays gadget state on the player's screen.
- It should show selected gadget feedback, availability, and active state where supported.
- It is client-side presentation. The HUD tells the player what the local client believes is happening, while the server or gameplay logic may still control actual effects.
- HUD art and color should come from the source assets instead of being recolored through fragile script-side tint workarounds.

What mission makers should know:

| HUD detail | Meaning |
| --- | --- |
| Selected gadget | Shows which gadget the player is currently controlling. |
| Ready state | Communicates whether the gadget can be used. |
| Active state | Communicates whether a shield, effect, or temporary gadget mode is currently active. |
| Cooldown or unavailable feedback | Helps players understand why activation did not happen. |

Testing checklist:

- Equip each gadget through the normal inventory path.
- Confirm the gadget appears in Arsenal or mission loadout where intended.
- Confirm selection and activation update the HUD.
- Confirm multiplayer behavior with at least host and client.
- Confirm packed PBO behavior, not only loose-file editor behavior.
