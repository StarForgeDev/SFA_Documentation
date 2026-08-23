---
title: Modules
---

# SFA Modules

The SFA module addon registers Eden modules under the `SFA Modules` category. These pages are written for mission makers first, then maintainers.

## Module Index

| Module | Class | Purpose |
| --- | --- | --- |
| Zero-G Area | `SFA_Module_ZeroG` | Creates a configurable low-gravity or zero-gravity zone. |
| KOTOR Dialogue NPC | `SFA_Module_KotorDialogue` | Adds interactive dialogue to a synced NPC. |
| KOTOR Dialogue Object | `SFA_Module_KotorDialogueObject` | Adds dialogue to an object, with optional remote speaker behavior. |
| KOTOR Dialogue Set | `SFA_Module_KotorDialogueSet` | Defines dialogue text, sounds, options, branches, and auto-continue behavior. |
| KOTOR Dialogue Event | `SFA_Module_KotorDialogueEvent` | Runs server-side effects when dialogue reaches a selected point. |
| KOTOR Objective Event | `SFA_Module_KotorObjectiveEvent` | Watches objective variables or damage conditions and completes mission logic. |
| Keypad Door Lock | `SFA_Module_KeypadLock` | Adds a keypad interaction to lock or unlock synced doors. |
| Kessel Sabacc Table | `SFA_Module_KesselSabacc` | Creates or manages an interactable Sabacc table. |
| Convoy | `SFA_Module_Convoy` | Spawns and routes a convoy, optionally with reinforcements. |
| Occupation Zone | `SFA_Module_Occupation` | Populates an area with patrols, garrisons, vehicles, static weapons, checkpoints, and reinforcements. |
| Ambient Civilian | `SFA_Module_AmbientCivilian` | Adds ambient pedestrians, traffic, police, and cleanup behavior. |
| Intro Text | `SFA_Module_IntroText` | Displays stylized mission intro text with optional sound. |
| Cinematic Border | `SFA_Module_CinematicBorder` | Adds cinematic letterbox bars and optional title text. |
| Trap / Alarm Inventory | `SFA_Module_InventoryTrap` | Triggers alarms, variables, code, damage, or explosions when inventory is opened or looted. |

## Recommended Page Format

Every module page should eventually include:

- Location in Eden
- What to sync
- Required attributes
- Optional attributes
- Multiplayer locality notes
- Example setup
- Known limitations
- Test status

## Pages

- [Zero-G Area](./zero-g/)
- [KOTOR Dialogue](./kotor-dialogue/)
- [Keypad Door Lock](./keypad-lock/)
- [Kessel Sabacc](./kessel-sabacc/)
- [Convoy and Occupation](./convoy-occupation/)
- [Ambient and Cinematic Modules](./ambient-cinematic/)
- [Trap / Alarm Inventory](./trap-inventory/)
