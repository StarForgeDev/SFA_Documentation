---
title: KOTOR Dialogue
---

# KOTOR Dialogue

Main classes:

- `SFA_Module_KotorDialogue`
- `SFA_Module_KotorDialogueObject`
- `SFA_Module_KotorDialogueSet`
- `SFA_Module_KotorDialogueEvent`
- `SFA_Module_KotorObjectiveEvent`

The KOTOR Dialogue modules create branching NPC or object conversations with optional camera behavior, voice playback, objective events, and server-side mission logic.

## Basic NPC Setup

1. Place an NPC.
2. Place `KOTOR Dialogue NPC`.
3. Sync the module to the NPC.
4. Set the speaker name, action title, starting set ID, and camera settings.
5. Place one or more `KOTOR Dialogue Set` modules.
6. Give each dialogue set a unique Set ID.
7. Sync the dialogue sets into the dialogue NPC module.

## Object Setup

Use `KOTOR Dialogue Object` when the interaction belongs to an object instead of a living speaker. It supports remote speaker fields, which are useful for comm panels, droids, terminals, or an off-screen commander.

## Dialogue Sets

Each `KOTOR Dialogue Set` can define:

- NPC dialogue text
- NPC sound path
- Auto-continue behavior
- Next set ID
- Up to four player options
- Per-option player sound
- Per-option response text
- Per-option response sound
- Per-option next set ID
- Whether an option closes the dialogue

## Dialogue Events

Use `KOTOR Dialogue Event` to run logic when a conversation reaches a specific state. It can set variables, trigger variables, run server code, and optionally switch the speaker or group hostile.

Use `KOTOR Objective Event` to monitor objective state. It can watch a variable, damage threshold, required variable, and completion behavior.

## Multiplayer Notes

Previous source work used a client-local action pattern for visible interactions while keeping shared state server-owned. Runtime verification is still required for each mission, especially for JIP clients and dedicated servers.

## Example Branch

| Set ID | Text | Options |
| --- | --- | --- |
| `start` | "Identify yourself." | `Republic patrol`, `Just passing through`, `Attack` |
| `republic` | "Then you know the passcode." | Continue to `passcode` |
| `passcode` | "Speak it." | Correct answer sets `door_unlocked`; wrong answer closes or triggers hostile event. |

## Test Status

Source-level documentation exists. Confirm action visibility, dialogue flow, camera behavior, sounds, event firing, and objective variables in the target mission.
