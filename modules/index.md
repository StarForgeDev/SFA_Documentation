---
title: Modules
---

# SFA Modules

StarForge modules are Eden-placeable mission systems. Mission makers place them in Eden, configure their attributes, and sync them to the objects, units, zones, or logic pieces they control. Each module page below explains what the module is, how it works, and what each configurable setting changes.

<div class="status-strip compact">
  <span><strong>Category:</strong> SFA Modules</span>
  <span><strong>Audience:</strong> Eden mission makers</span>
  <span><strong>Source:</strong> SFA_Modules</span>
</div>

## Module Index

| Module | Class | Purpose |
| --- | --- | --- |
| [Zero-G Area](./zero-g/) | `SFA_Module_ZeroG` | Creates a configurable low-gravity or zero-gravity movement zone. |
| [Ambient Air Battle](./ambient-air-battle/) | `SFA_Module_AmbientAirBattle` | Creates a cinematic aircraft or starfighter battle around the mission area. |
| [Ambient Battle](./ambient-battle/) | `SFA_Module_AmbientBattle` | Creates a configurable ground battle with infantry, vehicles, and hostility settings. |
| [Ambient Civilian](./ambient-civilian/) | `SFA_Module_AmbientCivilian` | Adds pedestrians, traffic, police, cleanup behavior, and class-list controlled civilian ambience. |
| [Intro Text](./intro-text/) | `SFA_Module_IntroText` | Displays stylized mission intro text with fonts, colors, timing, fade, and optional sound. |
| [Cinematic Border](./cinematic-border/) | `SFA_Module_CinematicBorder` | Adds letterbox bars and optional title/subtitle text for cinematic moments. |
| [KOTOR Dialogue NPC](./kotor-dialogue/) | `SFA_Module_KotorDialogue` | Adds the player interaction and main branching dialogue controller to a synced NPC. |
| [KOTOR Dialogue Object](./kotor-dialogue-object/) | `SFA_Module_KotorDialogueObject` | Lets an object act as a dialogue speaker or remote speaker source. |
| [KOTOR Dialogue Set](./kotor-dialogue-set/) | `SFA_Module_KotorDialogueSet` | Defines one dialogue node with NPC text, sounds, player options, branches, and final-option behavior. |
| [KOTOR Dialogue Event](./kotor-dialogue-event/) | `SFA_Module_KotorDialogueEvent` | Fires mission logic when dialogue reaches a selected point. |
| [KOTOR Objective Event](./kotor-objective-event/) | `SFA_Module_KotorObjectiveEvent` | Watches variables or damage conditions and completes objective-style logic. |
| [Keypad Door Lock](./keypad-lock/) | `SFA_Module_KeypadLock` | Adds a keypad interaction to lock, unlock, relock, or slice synced doors. |
| [Kessel Sabacc Table](./kessel-sabacc/) | `SFA_Module_KesselSabacc` | Creates or manages an interactable Sabacc table. |
| [Convoy](./convoy/) | `SFA_Module_Convoy` | Spawns and routes a vehicle convoy with optional escorts and reinforcements. |
| [Occupation Zone](./occupation/) | `SFA_Module_Occupation` | Populates an area with patrols, garrisons, vehicles, statics, checkpoints, and reinforcements. |
| [Trap / Alarm Inventory](./trap-inventory/) | `SFA_Module_InventoryTrap` | Triggers alarms, variables, server code, damage, or explosions when inventory is opened or looted. |

## How to Use These Pages

Each module page is written in the same format:

- what the module is for;
- how the module normally works in an Eden mission;
- what needs to be synced or configured;
- what each setting changes;
- practical mission-maker notes;
- runtime testing notes where the behavior depends on multiplayer, locality, UI scaling, AI pathing, or packed PBO behavior.
