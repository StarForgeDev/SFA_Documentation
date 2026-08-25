---
title: KOTOR Dialogue NPC
---

# KOTOR Dialogue NPC

Class: `SFA_Module_KotorDialogue`

Function: `SFA_fnc_moduleKotorDialogue`

[Back to Modules](../)

## What It Is

KOTOR Dialogue NPC is the main controller module for a branching conversation attached to a living NPC. It gives players an interaction action, opens the dialogue flow, starts at a configured dialogue set, and applies optional cinematic camera behavior.

Use it for quest givers, commanders, prisoners, merchants, informants, enemy officers, companions, and any NPC that should speak through a structured RPG-style conversation instead of a simple interaction line.

This module does not contain every dialogue line by itself. It points to one or more [KOTOR Dialogue Set](../kotor-dialogue-set/) modules, and those sets contain the NPC text, player options, responses, sounds, and branch destinations.

## How It Works

The mission maker places an NPC, places this module, and syncs the module to the NPC. When a player gets close enough, the configured action title appears. Activating the action starts the conversation at the configured Starting Set ID.

The module can optionally use a cinematic camera. Camera settings control distance, height, side offset, field of view, transition timing, and whether the view cuts back to the player when choices are shown.

The module is the entry point. The actual conversation path is controlled by dialogue set IDs. If the Starting Set ID does not match a real Dialogue Set, the conversation will not have a valid first node.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Action Title | Text shown to the player in the interaction menu. Use a clear label like `Talk`, `Question Officer`, or `Access Dialogue`. |
| Interaction Radius | Distance at which the player can start the dialogue. Larger values make interaction easier; smaller values force the player closer to the speaker. |
| Speaker Name | Name displayed for the NPC speaker. This should be the character name or role shown in the dialogue UI. |
| Starting Set ID | Dialogue set ID used as the first conversation node. This must match a KOTOR Dialogue Set. |
| Cinematic Camera | Enables or disables the camera presentation layer. |
| Camera Distance | How far the camera sits from the speaker. |
| Camera Height Offset | Vertical offset for the camera. Use this to frame tall or short characters. |
| Camera Side Offset | Horizontal offset for an over-the-shoulder or angled conversation view. |
| Camera FOV | Field of view used by the conversation camera. Lower values feel more zoomed-in; higher values show more of the scene. |
| Camera Transition Time | Time used to move into the dialogue camera. |
| Cut To Player For Options | Changes camera focus when player choices are displayed. |
| Reserved Camera Timing | Extra timing buffer used around camera transitions or option presentation. |
| Seconds Per Text Character | Controls auto-timing based on line length. Longer values give players more reading time. |
| Minimum Option Delay | Shortest delay before player options appear. |
| Maximum Option Delay | Longest delay before player options appear. |

## Basic Setup

1. Place the NPC.
2. Place `KOTOR Dialogue NPC`.
3. Sync the module to the NPC.
4. Set the speaker name and action title.
5. Set `Starting Set ID`, for example `start`.
6. Place a [KOTOR Dialogue Set](../kotor-dialogue-set/) with the same Set ID.
7. Add more Dialogue Set modules for branches.
8. Add [Dialogue Event](../kotor-dialogue-event/) or [Objective Event](../kotor-objective-event/) modules if the conversation should affect the mission.

## Related Modules

- [KOTOR Dialogue Object](../kotor-dialogue-object/)
- [KOTOR Dialogue Set](../kotor-dialogue-set/)
- [KOTOR Dialogue Event](../kotor-dialogue-event/)
- [KOTOR Objective Event](../kotor-objective-event/)

## Testing

Verify action visibility, starting set lookup, branching, camera behavior, sound playback, final options, event firing, and JIP behavior in the target mission environment.
