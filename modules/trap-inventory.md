---
title: Trap / Alarm Inventory
---

# Trap / Alarm Inventory

Class: `SFA_Module_InventoryTrap`

Function: `SFA_fnc_moduleInventoryTrap`

The Trap / Alarm Inventory module triggers mission effects when a synced container is opened, looted, or both.

## Basic Setup

1. Place a container or object with inventory.
2. Place `Trap / Alarm Inventory`.
3. Sync the module to the container.
4. Choose activation mode.
5. Configure recipients, alarm radius, messages, variables, server code, damage, or explosion behavior.

## Key Settings

| Setting | Property | Use |
| --- | --- | --- |
| Activate When | `SFA_InventoryTrap_ActivationMode` | Controls whether opening, item removal, or either action triggers the trap. |
| Execute Once Per Container | `SFA_InventoryTrap_ExecuteOnce` | Prevents repeated triggers. |
| Repeat Cooldown | `SFA_InventoryTrap_Cooldown` | Delay before the same container can trigger again. |
| Alarm Recipients | `SFA_InventoryTrap_RecipientMode` | Controls who receives the alarm. |
| Alarm Radius | `SFA_InventoryTrap_AlarmRadius` | Radius for nearby recipients. |
| Alarm Message | `SFA_InventoryTrap_AlarmMessage` | Message shown when triggered. |
| Alarm Sound Class | `SFA_InventoryTrap_AlarmSound` | Sound class played on trigger. |
| Set Variable Name | `SFA_InventoryTrap_SetVariable` | Variable set after trigger. |
| Trigger Variable Name | `SFA_InventoryTrap_TriggerVariable` | Variable watched or triggered by the trap. |
| Server Code | `SFA_InventoryTrap_ServerCode` | Server-side code executed on trigger. |
| Container Damage | `SFA_InventoryTrap_ContainerDamage` | Damage applied to the container. |
| Explosion Ammo Class | `SFA_InventoryTrap_ExplosionClass` | Ammo classname for explosion behavior. |

## Mission Ideas

- Alarmed supply cache
- Booby-trapped crate
- Evidence locker that sets an objective variable
- Loot container that alerts nearby guards

## Test Status

Verify locality, repeated trigger behavior, inventory removal detection, and server code execution in multiplayer.
