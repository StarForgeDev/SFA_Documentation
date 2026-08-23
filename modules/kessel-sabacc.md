---
title: Kessel Sabacc
---

# Kessel Sabacc Table

Class: `SFA_Module_KesselSabacc`

Function: `SFA_fnc_moduleKesselSabacc`

The Kessel Sabacc module creates or manages an interactable Sabacc table for roleplay and downtime scenes.

## Basic Setup

1. Place `Kessel Sabacc Table`.
2. Decide whether the module should create its own table prop.
3. Configure AI opponents, starting credits, buy-in, player table name, and interaction radius.
4. Test interaction from player and spectator/admin perspectives.

## Key Settings

| Setting | Property | Use |
| --- | --- | --- |
| AI Opponents | `SFA_KesselSabacc_AIOpponents` | Number of AI opponents at the table. |
| Starting Credits | `SFA_KesselSabacc_StartingCredits` | Player starting credits. |
| Hand Buy-In | `SFA_KesselSabacc_BuyIn` | Credit cost per hand. |
| Player Table Name | `SFA_KesselSabacc_PlayerName` | Display name used for the player at the table. |
| Create Table Prop | `SFA_KesselSabacc_CreateTable` | Spawns a table prop from the module. |
| Interaction Radius | `SFA_KesselSabacc_InteractionRadius` | Distance needed to join or interact. |

## Mission Use

Good fits:

- Cantina scenes
- Downtime between objectives
- Smuggler or underworld hubs
- Optional credit-based side activities

## Test Status

Needs runtime verification for UI flow, credit persistence, reconnect behavior, and multiplayer table ownership.
