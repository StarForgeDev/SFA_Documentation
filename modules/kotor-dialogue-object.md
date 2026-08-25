---
title: KOTOR Dialogue Object
---

# KOTOR Dialogue Object

Class: `SFA_Module_KotorDialogueObject`

Function: `SFA_fnc_moduleKotorDialogueObject`

[Back to Modules](../)

## What It Is

KOTOR Dialogue Object lets a non-living object participate in the dialogue system. It is useful for terminals, comm panels, droids represented by props, hologram devices, doors, consoles, briefing tables, and remote speakers.

Use it when the player should interact with an object but the dialogue should still feel like a conversation.

## How It Works

The object module identifies or configures an object as a dialogue-capable speaker. It can point to a remote speaker variable and speaker name, which lets a physical object act as the interaction point while the voice or character identity belongs to someone else.

Example: a player uses a shipboard comm terminal, but the displayed speaker is a Republic commander speaking remotely.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Remote Speaker Variable | Variable name used to locate the remote speaker object or unit. This is useful when the interaction object and speaker identity are separate. |
| Remote Speaker Name | Name shown for the remote speaker. Use this for comms, holograms, and off-screen characters. |
| Play Voice From Remote | Controls whether voice playback should come from the remote speaker source instead of the local object. |

## Mission-Maker Notes

- Use object dialogue for terminals and comms instead of forcing invisible NPCs into the scene.
- Give the object a clear placement and interaction radius through the related dialogue setup.
- If voice playback matters spatially, test whether it should sound like it comes from the object or the remote speaker.

## Example Uses

- Holo terminal that connects to a fleet officer.
- Locked door panel that speaks as a security AI.
- Astromech terminal that plays dialogue from a hidden droid.
- Hologram projector used for mission briefing dialogue.

## Testing

Verify remote speaker lookup, voice playback origin, action visibility, and whether every client sees the same speaker name and dialogue state.
