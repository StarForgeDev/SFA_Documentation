---
title: Kessel Sabacc
---

# Kessel Sabacc Table

Class: `SFA_Module_KesselSabacc`

Function: `SFA_fnc_moduleKesselSabacc`

The Kessel Sabacc module creates or manages an interactable Sabacc table for roleplay and downtime scenes.

## What It Is

Kessel Sabacc Table is a social gameplay module. It gives players an interactable Sabacc table that can be used for cantina scenes, underworld hubs, gambling encounters, downtime between objectives, or mission beats where credits and social interaction matter.

It is not a combat module. Its value is giving the mission a Star Wars activity that players can interact with instead of only walking through a static set piece.

## How It Works

The module either controls an existing table setup or creates a table prop if configured to do so. Players interact inside the configured radius. The table uses starting credits, hand buy-in, and AI opponent settings to define the game environment.

The player table name controls how the player's seat or table presence is labeled. AI opponent count controls whether the table feels empty, casual, or busy.

## Basic Setup

1. Place `Kessel Sabacc Table`.
2. Decide whether the module should create its own table prop.
3. Configure AI opponents, starting credits, buy-in, player table name, and interaction radius.
4. Test interaction from player and spectator/admin perspectives.

## What Can Be Changed

| Setting | Property | Use |
| --- | --- | --- |
| AI Opponents | `SFA_KesselSabacc_AIOpponents` | Number of AI opponents at the table. Higher values make the table feel more populated. |
| Starting Credits | `SFA_KesselSabacc_StartingCredits` | Credits available to the player when using the table. Use this to control how generous or risky the activity feels. |
| Hand Buy-In | `SFA_KesselSabacc_BuyIn` | Credit cost per hand. Higher buy-ins make each hand more important. |
| Player Table Name | `SFA_KesselSabacc_PlayerName` | Display name used for the player at the table. |
| Create Table Prop | `SFA_KesselSabacc_CreateTable` | Spawns a table prop from the module. Disable this if you already placed a custom table. |
| Interaction Radius | `SFA_KesselSabacc_InteractionRadius` | Distance needed to join or interact. Larger values are easier to use; smaller values require players to stand closer. |

## Mission Use

Good fits:

- Cantina scenes
- Downtime between objectives
- Smuggler or underworld hubs
- Optional credit-based side activities

## Test Status

Needs runtime verification for UI flow, credit persistence, reconnect behavior, and multiplayer table ownership.
