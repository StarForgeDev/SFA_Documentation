---
title: Medical, Boosts, and Grenades
---

# Medical, Boosts, and Grenades

Folders:

- `SFA_Medical`
- `SFA_Boosts`
- `SFA_Grenades`

These addons provide consumables, healing tools, enhancement stims, and throwable effects.

## Medical Items

Important medical classes include:

- `SFA_Base_Stim`
- `SFA_Kolto_Stim`
- `SFA_Polybiotic_Stim`
- `SFA_Kyrprax_Stim`
- `SFA_Anodyne_Stim`
- `SFA_Battle_Stim`
- `SFA_Parallactic_Stim`
- `SFA_BactaIV_250`
- `SFA_BactaIV_500`
- `SFA_BactaIV_1000`

## Boost Items

Important boost classes include:

- `SFA_EnergizedKoltoStim`
- `SFA_AdvancedKoltoStim`
- `SFA_AdvancedReflexStim`

Boosts use functions under the `SFA_Boosts` function namespace.

## Grenades

Important grenade ammo and magazine classes include:

- `SFA_Sticky_Grenade_Ammo`
- `SFA_Sonic_Grenade_Ammo`
- `SFA_Flashbang_Grenade_Ammo`
- `SFA_Imploder_Grenade_Ammo`
- `SFA_CryoGrenade_Ammo_test`
- `SFA_KoltoGrenade_Ammo`
- `SFA_PoisonKoltoGrenade_Ammo`
- `SFA_Sticky_Grenade_Mag`
- `SFA_Sonic_Grenade_Mag`
- `SFA_Flashbang_Grenade_Mag`
- `SFA_Imploder_Grenade_Mag`
- `SFA_CryoGrenadeMag`
- `SFA_KoltoGrenadeMag`
- `SFA_KoltoPoisonGrenadeMag`

## Runtime Checks

- Confirm ACE medical integration for each healing item.
- Confirm throw muzzle availability in Arsenal and mission loadouts.
- Confirm grenade effects happen on the correct machine in multiplayer.
- Confirm projectile tracking uses the actual projectile object, not only fired event metadata.
