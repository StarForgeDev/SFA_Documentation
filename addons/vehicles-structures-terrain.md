---
title: Vehicles, Structures, and Terrain
---

# Vehicles, Structures, and Terrain

Folders:

- `SFA_Vehicles_R`
- `SFA_Vehicles_S`
- `SFA_Vehicles_N`
- `SFA_Vehicles_R_Driverless`
- `SFA_Droid_MKIV`
- `SFA_Structures`
- `SFA_Structures_Core`
- `SFA_Structures_Pirate`
- `SFA_Terrain_Caves`
- `SFA_Terrain_Rocks`
- `SFA_Terrain_Trenches`
- `SFA_Ground_Decals`
- `SFA_Manaan`
- `SFA_Ossus`
- `SFA_Umbara_Air`

## Vehicles

Vehicle documentation should include:

- Vehicle classname
- Faction
- Crew positions
- Turrets
- Weapons and magazines
- Animation source notes
- Known model memory points
- Tested maps and use cases

## Structures

Structure documentation should include:

- Editor category and subcategory
- Whether the object is simple object compatible
- Whether it has doors, actions, sounds, damage, or animations
- Known placement restrictions

## Terrain Assets

Terrain documentation should include:

- Object classnames
- Terrain Builder usage notes
- Roadway, geometry, fire geometry, and view geometry notes
- Known packing requirements

## Runtime Checks

- Drive or fly vehicles in-game after model or config changes.
- Test turrets, optics, muzzle memory points, and animation axes.
- Test structures in Eden, Zeus, and packed PBO form.
- Test terrain objects for collision, AI pathing, and visual LOD behavior.
