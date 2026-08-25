---
title: Trap / Alarm Inventory
---

# Trap / Alarm Inventory

Class: `SFA_Module_InventoryTrap`

Function: `SFA_fnc_moduleInventoryTrap`

The Trap / Alarm Inventory module triggers mission effects when a synced container is opened, looted, or both.

## What It Is

Trap / Alarm Inventory turns a container into a mission event source. It can represent a booby-trapped cache, alarmed evidence locker, monitored supply crate, rigged corpse inventory, stolen-object trigger, or explosive loot trap.

Use it when player inventory interaction should have consequences.

## How It Works

The mission maker syncs the module to a container or inventory-capable object. The module watches for the configured activation behavior, such as opening the inventory, removing an item, or either action. When triggered, it can show alarm messages, play a sound, set variables, run server code, damage the container, or create an explosion using a configured ammo class.

Cooldown and execute-once settings control whether the trap is a single-use event or a repeatable alarm system.

## Basic Setup

1. Place a container or object with inventory.
2. Place `Trap / Alarm Inventory`.
3. Sync the module to the container.
4. Choose activation mode.
5. Configure recipients, alarm radius, messages, variables, server code, damage, or explosion behavior.

## What Can Be Changed

| Setting | Property | Use |
| --- | --- | --- |
| Activate When | `SFA_InventoryTrap_ActivationMode` | Controls whether opening, item removal, or either action triggers the trap. Opening is good for alarms; removal is good for theft detection. |
| Execute Once Per Container | `SFA_InventoryTrap_ExecuteOnce` | Prevents repeated triggers. Use this for explosions or objective variables. |
| Repeat Cooldown | `SFA_InventoryTrap_Cooldown` | Delay before the same container can trigger again. Use for repeatable alarms. |
| Alarm Recipients | `SFA_InventoryTrap_RecipientMode` | Controls who receives the alarm notification. |
| Alarm Radius | `SFA_InventoryTrap_AlarmRadius` | Radius for nearby recipients or alert behavior. |
| Alarm Message | `SFA_InventoryTrap_AlarmMessage` | Message shown when triggered. |
| Alarm Sound Class | `SFA_InventoryTrap_AlarmSound` | Sound class played on trigger. |
| Set Variable Name | `SFA_InventoryTrap_SetVariable` | Variable set after trigger. Use it to advance objectives or unlock other logic. |
| Trigger Variable Name | `SFA_InventoryTrap_TriggerVariable` | Variable watched or triggered by the trap. |
| Server Code | `SFA_InventoryTrap_ServerCode` | Server-side code executed on trigger. Use for custom mission actions. |
| Container Damage | `SFA_InventoryTrap_ContainerDamage` | Damage applied to the container. |
| Explosion Ammo Class | `SFA_InventoryTrap_ExplosionClass` | Ammo classname used for explosion behavior. Test blast size before using near objectives. |

## Mission Ideas

- Alarmed supply cache
- Booby-trapped crate
- Evidence locker that sets an objective variable
- Loot container that alerts nearby guards

## Test Status

Verify locality, repeated trigger behavior, inventory removal detection, and server code execution in multiplayer.
