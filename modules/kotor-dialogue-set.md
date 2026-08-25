---
title: KOTOR Dialogue Set
---

# KOTOR Dialogue Set

Class: `SFA_Module_KotorDialogueSet`

Function: handled by the KOTOR dialogue system

[Back to Modules](../)

## What It Is

KOTOR Dialogue Set is one conversation node. It contains the NPC line, optional voice, auto-continue behavior, and up to four player options. Each option can have its own player sound, response text, response sound, next set ID, and final-dialogue behavior.

Use one Dialogue Set for each meaningful step in a conversation. A full conversation is usually a chain or tree of multiple Dialogue Set modules connected by set IDs.

## How It Works

The NPC or Object dialogue module starts at a Set ID. The matching Dialogue Set displays its NPC line. The player then sees the available options unless the set is configured to auto-continue. When the player chooses an option, the system can show a response and then move to another set ID or close the conversation.

Dialogue Set modules are the backbone of branching conversations. If a next set ID points to a set that does not exist, that branch will fail or stop.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Set ID | Unique ID for this conversation node. Other modules and options use this value to jump to this node. |
| NPC Dialogue Text | Main line spoken or displayed by the NPC/object for this node. |
| NPC Sound Path | Optional sound played with the NPC line. Use for voiced dialogue. |
| Auto Continue To Next Set | Skips player options and automatically advances to another Set ID. Good for monologues or timed briefings. |
| Continue To Set ID | Destination used when auto-continue is enabled. |
| Option Text | Player choice text. Each set supports up to four options. |
| Option Sound | Optional sound for the player's selected line. |
| Response Text | NPC response after the player chooses that option. |
| Response Sound | Optional sound for the response. |
| Next Set ID | Dialogue set loaded after the response. Use this to branch or loop. |
| Is Final Dialogue | Closes the conversation after that option/response instead of continuing. |

## Branching Pattern

| Set ID | Purpose |
| --- | --- |
| `start` | First line and broad choices. |
| `ask_job` | Explains the mission or objective. |
| `ask_reward` | Optional reward or negotiation branch. |
| `accept` | Player accepts and triggers mission state. |
| `decline` | Player exits or delays the objective. |

## Testing

Walk every branch manually. Confirm each option reaches the intended next set, final options close properly, sounds play, and no branch points to a missing Set ID.
