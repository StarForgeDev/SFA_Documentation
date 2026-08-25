---
title: Keypad Door Lock
---

# Keypad Door Lock

Class: `SFA_Module_KeypadLock`

Function: `SFA_fnc_moduleKeypadLock`

The Keypad Door Lock module adds a keypad-style lock interaction for doors or synced objects.

## What It Is

Keypad Door Lock is an access-control module. It gives a door, keypad object, or synced object a password/slicing interaction so mission makers can create locked rooms, secure hangars, evidence lockers, prison cells, objective gates, and puzzle doors.

It is designed for mission flow control. The keypad can block players until they find a code, slice the lock, complete an objective, or trigger a scripted unlock.

## How It Works

The mission maker syncs the module to the door or keypad setup. The module exposes an interaction inside the configured radius. When players enter the correct password or complete the configured slicing behavior, the module controls the target door action numbers.

Door Action Numbers matter because Arma buildings and custom structures can use different animation/action indexes for their doors. A valid password with the wrong door index can appear to work while the wrong part of the object animates or nothing visible happens.

## Basic Setup

1. Place the door or object that should be locked.
2. Place `Keypad Door Lock`.
3. Sync the module to the door or object.
4. Configure the password.
5. Configure the door action numbers if the target object uses specific door animation/action indexes.

## What Can Be Changed

| Setting | Property | Use |
| --- | --- | --- |
| Synced to Keypad | `SFA_KeypadLock_SyncedToKeypad` | Uses a synced keypad object instead of only direct door interaction. Use this when the keypad mesh is separate from the door. |
| Keypad Variable | `SFA_KeypadLock_KeypadVariable` | Variable name for identifying a keypad object. This helps when scripts or other modules need to reference the same keypad. |
| Password | `SFA_KeypadLock_Password` | Code players must enter. Use mission clues, datapads, dialogue, or objectives to reveal it. |
| Relock Mode | `SFA_KeypadLock_RelockMode` | Determines if and when the door locks again. Use relocking for stealth/security missions and permanent unlock for progression doors. |
| Interaction Radius | `SFA_KeypadLock_InteractionRadius` | Distance at which the interaction is available. Increase it for awkward objects; decrease it for precise panel use. |
| Slice Seconds | `SFA_KeypadLock_SliceSeconds` | Time required for slicing/hacking behavior. Longer times create vulnerability during combat or stealth. |
| Door Action Numbers | `SFA_KeypadLock_DoorIndices` | Door action indexes used by the target object. These are model-specific and must be tested per structure. |

## Usage Notes

- Door index values are model-specific. If the wrong index is used, the keypad may work but the expected door animation will not.
- For multiplayer missions, verify that all clients see the correct lock state after unlock, relock, and JIP.

## Test Status

Needs per-object runtime verification because Arma door actions differ by model.
