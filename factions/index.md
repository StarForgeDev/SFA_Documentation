---
title: Factions
---

# StarForge Factions

This page lists the StarForge faction classes and their Arma side. In Arma config, side `0` is OPFOR, side `1` is BLUFOR, and side `2` is INDFOR.

## Faction Classes

| Faction classname | Display name | Arma side |
| --- | --- | --- |
| `SFA_Republic` | `[SFA] Galactic Republic Military` | BLUFOR |
| `SFA_Republic_KOTOR` | `[SFA] Republic Military [KOTOR]` | BLUFOR |
| `SFA_Telos` | `[SFA] Telos Security Forces` | BLUFOR |
| `SFA_Umbaran` | `[SFA] Umbaran Defense Force` | BLUFOR |
| `SFA_Empire` | `[SFA] Reconstituted Sith Empire` | OPFOR |
| `SFA_Empire_KOTOR` | `[SFA] Sith Empire [KOTOR]` | OPFOR |
| `SFA_Revanites` | `[SFA] Revanite Coup` | OPFOR in faction config |
| `SFA_Rakghoul_Rep` | `[SFA] Rakghoul Plague Republic` | OPFOR |
| `SFA_Geonosian` | `[SFA] Geonosian Warband` | OPFOR |
| `SFA_Mantellian_Separatist` | `[SFA] Mantellian Separatists` | OPFOR |
| `SFA_Mandalorian_Mercs` | `[SFA] Mandalorian Clans` | INDFOR |
| `SFA_Mandalorian_Neo` | `[SFA] Mandalorian Neo-Crusaders` | INDFOR |
| `SFA_Onderon` | `[SFA] Onderonian Military` | INDFOR |
| `SFA_Czerka` | `[SFA] Czerka Corp` | INDFOR |
| `SFA_HuttCartel` | `[SFA] Hutt Cartel` | INDFOR |

## Specific Unit Groups

These are the visible unit group or subcategory names currently used by StarForge. Use these names when documenting Eden placement, Zeus composition, screenshots, and mission templates.

### Galactic Republic / BLUFOR

| Unit group | Parent faction | Side | Notes |
| --- | --- | --- | --- |
| `SFA_Infantry_taris` - Taris Reclamation Force | `SFA_Republic` | BLUFOR | Republic troops themed for Taris reclamation missions. |
| `SFA_Infantry_hoth` - 18th Hoth Garrison | `SFA_Republic` | BLUFOR | Cold-weather Republic defense force. Use for Hoth base defense, snow patrols, and frozen-front scenarios. |
| `SFA_Infantry_Ald` - 1st Alderaan Support Division | `SFA_Republic` | BLUFOR | Alderaan-themed Republic support troops. |
| `SFA_Havoc` - Havoc Squad | `SFA_Republic` | BLUFOR | Special operations unit category. |
| `SFA_CDF` - Coruscant Defense Force | `SFA_Republic` | BLUFOR | Urban security and defense unit category. |
| `SFA_301stID` - 301st Infantry Division | `SFA_Republic` | BLUFOR | Republic infantry division category. |
| `SFA_81stID` - 81st Infantry Division | `SFA_Republic` | BLUFOR | Republic infantry division category. |
| `SFA_86thID` - 86th Infantry Division | `SFA_Republic` | BLUFOR | Republic infantry division category. |
| `SFA_45thID` - 45th Infantry Division | `SFA_Republic` | BLUFOR | Republic infantry division category. |
| `SFA_Trandoshan_Partisan` - Trandoshan Partisans | `SFA_Republic` | BLUFOR | Republic-aligned Trandoshan unit category. |
| `SFA_Umbarans` - Umbaran Defense Force | `SFA_Umbaran` | BLUFOR | Umbaran defense troops. |

### Sith Empire / OPFOR

| Unit group | Parent faction | Side | Notes |
| --- | --- | --- | --- |
| Reconstituted Sith Empire | `SFA_Empire` | OPFOR | Main Sith Empire enemy force. |
| Sith Empire KOTOR | `SFA_Empire_KOTOR` | OPFOR | KOTOR-era Sith Empire troops. |
| Mantellian Separatists | `SFA_Mantellian_Separatist` | OPFOR | Separatist enemy troops. |
| Rakghoul Plague Republic | `SFA_Rakghoul_Rep` | OPFOR | Infected or plague-aligned hostile force. |
| Geonosian Warband | `SFA_Geonosian` | OPFOR | Hostile Geonosian force in faction config. |

### Independent / INDFOR

| Unit group | Parent faction | Side | Notes |
| --- | --- | --- | --- |
| Mandalorian Clans | `SFA_Mandalorian_Mercs` | INDFOR | Independent Mandalorian mercenary forces. |
| Mandalorian Neo-Crusaders | `SFA_Mandalorian_Neo` | INDFOR | Neo-Crusader era Mandalorian forces. |
| Onderonian Military | `SFA_Onderon` | INDFOR | Onderon military units. |
| Czerka Corp | `SFA_Czerka` | INDFOR | Corporate security and contractor units. |
| Hutt Cartel | `SFA_HuttCartel` | INDFOR | Hutt-aligned criminal or mercenary forces. |

## Notes for Mission Makers

- Use the faction classname when placing units through scripts, configs, or curator filtering.
- Use the visible unit group name when describing a mission setup to players or Zeus operators.
- If a unit class overrides side differently from its faction class, trust the unit class in-game and document the exception on the mission page.
