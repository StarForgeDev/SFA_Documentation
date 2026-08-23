---
title: Home
---

# StarForge Armory Documentation

This site documents the StarForge Armory Arma 3 addon set, with a focus on usable module instructions, mission-maker workflows, and source-level notes that help maintain the project.

This is an early documentation draft. It is meant to be expanded as modules are tested in Eden, hosted multiplayer, and packed PBO builds.

<div class="grid">
  <section class="card">
    <h3>Modules</h3>
    <p>Eden-placeable tools such as Zero-G, KOTOR Dialogue, Keypad Locks, Convoys, Occupation Zones, Kessel Sabacc, and cinematic helpers.</p>
    <p><a href="./modules/">Open module docs</a></p>
  </section>
  <section class="card">
    <h3>Addons</h3>
    <p>High-level package notes for SFA Core, equipment, weapons, gadgets, medical items, grenades, vehicles, structures, terrain, races, and units.</p>
    <p><a href="./addons/">Open addon docs</a></p>
  </section>
  <section class="card">
    <h3>Classnames</h3>
    <p>Starter reference for important faction, module, gadget, grenade, medical, and item classnames.</p>
    <p><a href="./reference/classnames/">Open classname reference</a></p>
  </section>
</div>

## Current Source Snapshot

The first pass was based on the local `SFA_Main` checkout. It includes these major source folders:

- `SFA_Core`
- `SFA_Modules`
- `SFA_Gadgets`
- `SFA_Gadgets_ACE`
- `SFA_Grenades`
- `SFA_Boosts`
- `SFA_Medical`
- `SFA_Equipment_R`, `SFA_Equipment_S`, `SFA_Equipment_N`, `SFA_Equipment_Geo`, `SFA_Equipment_Seps`, `SFA_Equipment_Misc`
- `SFA_Weapons_R`, `SFA_Weapons_S`, `SFA_Weapons_N`, `SFA_Weapons_Melee`, `SFA_Weapons_Core`
- `SFA_Vehicles_R`, `SFA_Vehicles_S`, `SFA_Vehicles_N`, `SFA_Vehicles_R_Driverless`
- `SFA_Structures`, `SFA_Structures_Core`, `SFA_Structures_Pirate`
- `SFA_Terrain_Caves`, `SFA_Terrain_Rocks`, `SFA_Terrain_Trenches`
- `SFA_Races`, `SFA_Units`, `SFA_Plague`, `SFA_Plague_Equipment`

## Documentation Rule

Separate source facts from runtime claims. If a page says a module config exposes a setting, that can be verified from source. If a page says a feature works in hosted multiplayer, dedicated server, Zeus, or JIP, that should be verified in game and noted with the test environment.
