---
title: Equipment and Units
---

# Equipment and Units

Folders:

- `SFA_Equipment_R`
- `SFA_Equipment_S`
- `SFA_Equipment_N`
- `SFA_Equipment_Geo`
- `SFA_Equipment_Seps`
- `SFA_Equipment_Misc`
- `SFA_Units`
- `SFA_Races`
- `SFA_Plague`
- `SFA_Plague_Equipment`

These packages provide faction equipment, unit classes, races, infected/plague content, and Eden group definitions.

## Faction Mapping Rule

When assigning units or vehicles to factions, use the exact existing faction class from `SFA_Core` when possible. Do not default everything to a generic neutral faction.

Examples:

- KOTOR Republic content should use `SFA_Republic_KOTOR`.
- KOTOR Sith content should use `SFA_Empire_KOTOR`.
- Revanite content should use `SFA_Revanites`.
- Hutt Cartel content should use `SFA_HuttCartel`.
- Rakghoul/plague content should use `SFA_Rakghoul_Rep`.
- Geonosian content should use `SFA_Geonosian`.
- Mantellian Separatist content should use `SFA_Mantellian_Separatist`.

## Unit Groups

`SFA_Units` contains group definitions for Republic, Empire, and Independent sides. Current groups include Republic Army variants, Special Operations Division, Sith Empire variants, KOTOR factions, Geonosians, Mantellian Separatists, and MKIV droid groups.

## Races

`SFA_Races` contains custom race and face content. Document each race with:

- Classnames
- Face texture variants
- Required materials
- Known visual limitations
- In-game screenshot checks

## Test Status

Equipment and unit documentation should be verified in Eden Arsenal, BI Arsenal, ACE Arsenal, Zeus, and faction/group browsers as appropriate.
