---
title: KOTOR Objective Event
---

# KOTOR Objective Event

Class: `SFA_Module_KotorObjectiveEvent`

Function: handled by the KOTOR objective/dialogue support system

[Back to Modules](../)

## What It Is

KOTOR Objective Event watches mission state and completes or advances objective-style logic. It can watch variables, damage thresholds, required variables, trigger variables, and server code.

Use it when a dialogue-related objective should complete because a condition becomes true, an object is damaged, a required variable is set, or another mission system reports success.

## How It Works

The module checks its configured condition at an interval. When the condition matches, it can set a completion variable, trigger another variable, and execute optional server code. Execute Once prevents repeated completion logic.

This module is useful when the conversation is only one part of the objective. For example, a player may accept a quest through dialogue, destroy a generator later, and then return to dialogue once a watched variable confirms the task is done.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Watched Variable Name | Variable the module monitors. This is the main condition source. |
| Complete When | Defines what watched state counts as complete. |
| Damage Threshold | Object damage value that can complete the objective when reached. |
| Required Variable Name | Extra variable that must be present or true before completion can happen. |
| Set Variable On Complete | Variable set after the objective condition completes. |
| Trigger Variable Name | Variable used to notify another system after completion. |
| Server Code | Optional server-side code executed when the objective completes. |
| Check Interval | How often the module checks the condition. Short intervals react faster; long intervals are cheaper. |
| Execute Once | Prevents repeated completion logic after the condition is met. |

## Example Uses

- Dialogue gives the objective, then the objective event waits for `generator_destroyed`.
- A door unlocks after an object reaches the damage threshold.
- A return-to-NPC branch becomes available after `sfa_intelRecovered` is set.
- Server code updates a task state after a watched variable is true.

## Testing

Verify the condition, interval timing, variable names, damage behavior, repeated execution, and whether the resulting objective state is visible for all clients and JIP players.
