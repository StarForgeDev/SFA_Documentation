---
title: Keypad Door Lock
---

# Keypad Door Lock

Class: `SFA_Module_KeypadLock`

Function: `SFA_fnc_moduleKeypadLock`

The Keypad Door Lock module adds a keypad-style lock interaction for doors or synced objects.

## Basic Setup

1. Place the door or object that should be locked.
2. Place `Keypad Door Lock`.
3. Sync the module to the door or object.
4. Configure the password.
5. Configure the door action numbers if the target object uses specific door animation/action indexes.

## Key Settings

| Setting | Property | Use |
| --- | --- | --- |
| Synced to Keypad | `SFA_KeypadLock_SyncedToKeypad` | Uses a synced keypad object instead of direct door interaction. |
| Keypad Variable | `SFA_KeypadLock_KeypadVariable` | Variable name for identifying a keypad object. |
| Password | `SFA_KeypadLock_Password` | Code players must enter. |
| Relock Mode | `SFA_KeypadLock_RelockMode` | Determines if and when the door locks again. |
| Interaction Radius | `SFA_KeypadLock_InteractionRadius` | Distance at which the interaction is available. |
| Slice Seconds | `SFA_KeypadLock_SliceSeconds` | Time required for slicing/hacking behavior, if used. |
| Door Action Numbers | `SFA_KeypadLock_DoorIndices` | Door action indexes used by the target object. |

## Usage Notes

- Door index values are model-specific. If the wrong index is used, the keypad may work but the expected door animation will not.
- For multiplayer missions, verify that all clients see the correct lock state after unlock, relock, and JIP.

## Test Status

Needs per-object runtime verification because Arma door actions differ by model.
