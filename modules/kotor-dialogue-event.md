---
title: KOTOR Dialogue Event
---

# KOTOR Dialogue Event

Class: `SFA_Module_KotorDialogueEvent`

Function: handled by the KOTOR dialogue system

[Back to Modules](../)

## What It Is

KOTOR Dialogue Event connects dialogue to mission logic. It lets a conversation set variables, trigger other systems, execute server code, or turn a speaker hostile when the dialogue reaches a selected point.

Use it when a conversation should unlock a door, start an ambush, complete an objective, reveal a marker, change reputation, spawn enemies, or switch an NPC from friendly to hostile.

## How It Works

The event watches the configured dialogue condition. When the conversation reaches the selected Set ID or event point, the event fires. Depending on configuration, it can set mission variables, trigger variable-based logic, execute server code, and change speaker/group behavior.

The Execute Once option is important. If the dialogue can be repeated, leaving Execute Once disabled may allow the same event to fire multiple times.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Fire Event When | Controls which dialogue moment causes the event to run. |
| Fire On Set ID | Specific dialogue Set ID that triggers the event. |
| Set Variable Name | Mission variable set when the event fires. Use this for triggers or other scripted checks. |
| Trigger Variable Name | Variable used to notify or trigger another mission system. |
| Server Code | Code executed on the server when the event fires. Use carefully and test on dedicated server. |
| Switch Speaker To Hostile | Turns the speaker hostile after the event. Good for failed negotiations or betrayal scenes. |
| Include Speaker Group | Applies hostility or behavior changes to the speaker's group, not only the individual speaker. |
| Execute Once | Prevents the same event from firing repeatedly. |

## Example Uses

- Choosing `I accept` sets `sfa_jobAccepted`.
- Choosing a threat option switches the NPC group hostile.
- Reaching `open_door` runs server-side code to unlock a door.
- Reaching `call_reinforcements` triggers a reinforcement module or script.

## Testing

Test every event path in multiplayer. Confirm variables are set where the rest of the mission expects them, server code runs only once when intended, and hostile switching is visible to all clients.
