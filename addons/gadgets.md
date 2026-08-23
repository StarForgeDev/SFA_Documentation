---
title: Gadgets
---

# SFA Gadgets

Folders:

- `SFA_Gadgets`
- `SFA_Gadgets_ACE`

The gadgets addon contains handheld or inventory-driven special tools and the gadget HUD.

## Current Gadgets

| Gadget | Class | Notes |
| --- | --- | --- |
| Wrist Rocket | `SFA_WristRocket_Gadget` | Gadget item with launcher, magazine, ammo, and function support. |
| Electro Dart | `SFA_ElectroDart_Gadget` | Stun or dart-style gadget with magazine and ammo support. |
| Concussive Missile | `SFA_ConcussiveMissile_Gadget` | Explosive or impact gadget with magazine and ammo support. |
| Energy Shield | `SFA_EnergyShield_Gadget` | Defensive timed shield behavior. |

## Shared Item Base

The source currently uses a shared gadget base:

- `SFA_Gadget_Base`
- `SFA_Gadget_ItemInfo`

The current direction is ordinary CBA miscellaneous inventory items, not medical items and not binocular-slot replacements.

## HUD

The gadget HUD is intended to show carried gadgets with readable status, charge, active state, role labels, icons, and progress bars.

Important setting:

- `SFA_GadgetHUD_Enabled`

## Runtime Checks

Before calling gadget work complete, verify:

- Item appears in BI Arsenal.
- Item appears in ACE Arsenal.
- Item can be added, removed, and selected.
- Item does not appear as a medical item unless intentionally configured.
- Keybinds do not conflict with expected controls.
- HUD hides when disabled, dead, map-open, or carrying no gadgets.
