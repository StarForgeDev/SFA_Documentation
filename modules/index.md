---
title: Modules
---

# SFA Modules

StarForge modules are Eden-placeable mission systems. Mission makers place them in Eden, set their attributes, and sync them to the objects or areas they control. Most modules are designed to let a mission maker build StarForge gameplay without manually wiring a large script system into the mission.

<div class="status-strip compact">
  <span><strong>Category:</strong> SFA Modules</span>
  <span><strong>Audience:</strong> Eden mission makers</span>
  <span><strong>Source:</strong> SFA_Modules</span>
</div>

## Module Index

| Module | Class | Purpose |
| --- | --- | --- |
| Zero-G Area | `SFA_Module_ZeroG` | Creates a configurable low-gravity or zero-gravity zone. |
| KOTOR Dialogue NPC | `SFA_Module_KotorDialogue` | Adds interactive dialogue to a synced NPC. |
| KOTOR Dialogue Object | `SFA_Module_KotorDialogueObject` | Adds dialogue to an object, with optional remote speaker behavior. |
| KOTOR Dialogue Set | `SFA_Module_KotorDialogueSet` | Defines dialogue text, sounds, options, branches, and auto-continue behavior. |
| KOTOR Dialogue Event | `SFA_Module_KotorDialogueEvent` | Runs server-side effects when dialogue reaches a selected point. |
| KOTOR Objective Event | `SFA_Module_KotorObjectiveEvent` | Watches objective variables or damage conditions and completes mission logic. |
| Keypad Door Lock | `SFA_Module_KeypadLock` | Adds a keypad interaction to lock or unlock synced doors. |
| Kessel Sabacc Table | `SFA_Module_KesselSabacc` | Creates or manages an interactable Sabacc table. |
| Convoy | `SFA_Module_Convoy` | Spawns and routes a convoy, optionally with reinforcements. |
| Occupation Zone | `SFA_Module_Occupation` | Populates an area with patrols, garrisons, vehicles, static weapons, checkpoints, and reinforcements. |
| Ambient Civilian | `SFA_Module_AmbientCivilian` | Adds ambient pedestrians, traffic, police, and cleanup behavior. |
| Intro Text | `SFA_Module_IntroText` | Displays stylized mission intro text with optional sound. |
| Cinematic Border | `SFA_Module_CinematicBorder` | Adds cinematic letterbox bars and optional title text. |
| Trap / Alarm Inventory | `SFA_Module_InventoryTrap` | Triggers alarms, variables, code, damage, or explosions when inventory is opened or looted. |

## Zero-G Area

`SFA_Module_ZeroG` creates a zero-gravity or low-gravity volume. It is meant for ship interiors, space walks, damaged stations, asteroid areas, or any mission space where normal Arma ground movement should be replaced by controlled drift.

How it works:

- The module defines an area where players, and optionally AI, are treated as being in a Zero-G zone.
- Movement is controlled through thrust values, maximum speeds, drift drag, boost behavior, roll speed, and recoil push.
- Magnetic floor clamping can let units stand or move on valid floor surfaces instead of floating at all times.
- The system should be treated as gameplay logic that needs live multiplayer testing for locality, JIP, headless client, and packed PBO behavior.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Enabled | Turns the zone on or off without deleting the module. |
| Thrust | Normal movement push while inside the zone. Higher values make movement more responsive. |
| Boost Thrust | Extra push applied while boosting. |
| Maximum Speed | Normal movement speed cap. |
| Boost Maximum Speed | Speed cap while boosting. |
| Drift Drag | How quickly floating movement slows down. Lower drag means players keep drifting longer. |
| Q/E Roll Speed | How quickly players roll while using roll controls. |
| Magnetic Floor Clamping | Enables floor attachment so players can walk on valid floor surfaces. |
| Floor Clamp Distance | How close a valid floor needs to be before clamping can happen. |
| Maximum Floor Slope | Prevents clamping to steep surfaces, walls, or ceilings. |
| Floor Jump Release Speed | How strongly the player is released from the floor when jumping. |
| Preserve Entry Momentum | Keeps player velocity when entering the zone instead of resetting movement. |
| Weapon Recoil Push | Lets weapon recoil move the player while floating. |
| Affect AI | Allows AI to be affected by the Zero-G system. |
| AI Arrival Radius | Controls how close AI needs to get before considering a movement target reached. |

## Ambient Air Battle

`SFA_Module_AmbientAirBattle` creates background starfighter or aircraft combat around the mission area. It is primarily a cinematic and ambience module, not a precision objective system.

How it works:

- The module spawns ships for two opposing sides.
- Aircraft operate inside a configurable battle volume.
- The mission maker controls how many ships spawn, how high the fight happens, how long it lasts, and which models are used.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Duration | How long the battle runs before cleanup or shutdown. |
| Unlimited Duration | Keeps the battle running without a normal time limit. |
| Ships Per Side | How many aircraft each side receives. |
| Spawn Radius | How far from the module aircraft can appear. |
| Travel Radius | How wide the combat movement area is. |
| Battle Height | Base altitude for the battle. |
| Height Spread | Vertical variation around the base height. |
| Ship Speed | Movement speed used by the spawned aircraft. |
| BLUFOR Model | Aircraft classname used for the friendly side. |
| REDFOR Model | Aircraft classname used for the hostile side. |

## Ambient Battle

`SFA_Module_AmbientBattle` creates a ground combat area with configurable sides, infantry groups, vehicles, and hostility settings. Use it for background fighting, moving front lines, or quick battlefield population.

How it works:

- The module spawns groups for enabled sides inside a defined battle radius.
- It can include BLUFOR, REDFOR, and GREENFOR at the same time.
- It can spawn vehicles in addition to infantry.
- It can force side hostility so the spawned groups fight without extra mission scripting.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Battle Radius | Size of the combat area around the module. |
| BLUFOR In Battle | Enables or disables BLUFOR participation. |
| REDFOR In Battle | Enables or disables OPFOR participation. |
| GREENFOR In Battle | Enables or disables INDFOR participation. |
| Groups Per Side | Number of infantry groups each enabled side receives. |
| Group Size | Number of units in each spawned infantry group. |
| BLUFOR Classes | Unit classnames used for BLUFOR spawns. |
| REDFOR Classes | Unit classnames used for OPFOR spawns. |
| GREENFOR Classes | Unit classnames used for INDFOR spawns. |
| Vehicles Per Side | Number of vehicles each side receives. |
| Force Side Hostility | Forces spawned sides to treat each other as enemies. |
| Duration | How long the battle remains active. |

## Ambient Civilian

`SFA_Module_AmbientCivilian` populates towns or settlements with civilian life. It supports pedestrians, traffic, police units, police vehicles, cleanup behavior, and spawn timing.

How it works:

- The module checks nearby players and eligible town areas.
- Civilians, traffic, and police can spawn around players while respecting minimum distance and cleanup distance.
- Custom class lists let the mission maker choose which civilians, vehicles, and police units appear.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Enable Pedestrians | Allows civilian foot traffic. |
| Enable Traffic | Allows civilian vehicles. |
| Max Pedestrians | Cap for active civilian pedestrians. |
| Max Traffic Vehicles | Cap for active traffic vehicles. |
| Enable Police | Allows police units and police vehicles. |
| Max Police | Cap for active police units. |
| Max Police Vehicles | Cap for active police vehicles. |
| Spawn Radius | Distance around players or towns where ambient units can spawn. |
| Min Player Distance | Prevents spawns too close to players. |
| Cleanup Distance | Removes ambient units once they are far enough away. |
| Spawn Interval | Delay between spawn checks. |
| Town Bias | Weights spawning toward town areas. |
| Civilian Classes | Civilian unit classnames. |
| Vehicle Classes | Civilian vehicle classnames. |
| Police Classes | Police unit classnames. |
| Police Vehicle Classes | Police vehicle classnames. |

## Cinematic Border

`SFA_Module_CinematicBorder` displays cinematic letterbox bars and optional title text. Use it for intros, cutscenes, dialogue moments, or objective transitions.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Show Border | Enables or disables the letterbox effect. |
| Border Size | Height of the cinematic bars. |
| Fade Time | How long the border takes to fade in or out. |
| Duration | How long the effect stays visible. |
| Title | Main text shown during the cinematic moment. |
| Subtitle | Secondary text shown under the title. |
| Title Size | Size of the main title. |
| Subtitle Size | Size of the subtitle. |
| Text Vertical Position | Vertical placement of the text on screen. |

## Intro Text

`SFA_Module_IntroText` displays formatted mission-opening text. It can show a title, subtitle, extra line, individual font settings, colors, timing, and an optional sound class.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Title / Subtitle / Additional Line | Text displayed to the player. |
| Font settings | Font family used for each line. |
| Font size settings | Screen size of each line. |
| Font color settings | Color of each line. |
| Fade In Time | How long the text takes to appear. |
| Visible Duration | How long the text remains visible. |
| Fade Out Time | How long the text takes to disappear. |
| Sound Class | Optional configured sound played with the intro. |

## KOTOR Dialogue

The KOTOR dialogue modules build branching Star Wars RPG-style conversations in Arma. The system is split into several module types so the mission maker can define a speaker, dialogue sets, responses, branching, events, and objective hooks.

Main pieces:

| Module | Class | What it does |
| --- | --- | --- |
| KOTOR Dialogue NPC | `SFA_Module_KotorDialogue` | Adds the player interaction and main dialogue controller to a synced NPC. |
| KOTOR Dialogue Object | `SFA_Module_KotorDialogueObject` | Uses an object as the dialogue speaker or remote speaker source. |
| KOTOR Dialogue Set | `SFA_Module_KotorDialogueSet` | Defines one dialogue node: NPC line, sounds, player options, responses, next set IDs, and final dialogue flags. |
| KOTOR Dialogue Event | `SFA_Module_KotorDialogueEvent` | Fires variables, trigger variables, server code, hostility changes, or group behavior when dialogue reaches a selected point. |
| KOTOR Objective Event | `SFA_Module_KotorObjectiveEvent` | Watches variables or damage thresholds and completes objective-style logic. |

What can be changed:

| Attribute group | What it changes |
| --- | --- |
| Action Title | Text shown on the interaction action. |
| Interaction Radius | Distance at which players can start dialogue. |
| Speaker Name | Name displayed for the speaker. |
| Starting Set ID | First dialogue set opened when conversation begins. |
| Camera settings | Cinematic camera distance, height offset, side offset, FOV, transition time, and whether to cut to the player for options. |
| Timing settings | Seconds per text character, minimum option delay, maximum option delay, and reserved camera timing. |
| Dialogue text | NPC text, player option text, response text, and final dialogue flags. |
| Dialogue sounds | NPC sound path, option sounds, and response sounds. |
| Branching | Continue-to set ID, option next set ID, auto-continue behavior, and final conversation behavior. |
| Event logic | Variables, trigger variables, server code, hostility switching, speaker group inclusion, and execute-once control. |
| Objective logic | Watched variable, completion condition, damage threshold, required variable, variable set on completion, check interval, and execute-once control. |

## Keypad Door Lock

`SFA_Module_KeypadLock` adds a keypad lock interaction to synced doors or keypad objects. It is for locked-door puzzles, slicing objectives, secure rooms, and mission progression gates.

How it works:

- The mission maker syncs the module to the target door or keypad setup.
- Players interact with the keypad and enter the configured password.
- The module can unlock, relock, run slicing timing, and control one or more door action numbers.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Synced to Keypad | Uses a synced keypad object instead of only the door target. |
| Keypad Variable | Variable name used to find or reference the keypad. |
| Password | Code players must enter. |
| Relock Mode | Controls if or how the door locks again. |
| Interaction Radius | Distance at which players can use the keypad. |
| Slice Seconds | Time required for slicing behavior. |
| Door Action Numbers | Door animation/action numbers controlled by the lock. |

## Kessel Sabacc Table

`SFA_Module_KesselSabacc` creates or manages an interactable Kessel Sabacc table for mission spaces that need a Star Wars gambling or social interaction scene.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| AI Opponents | Number of AI players at the table. |
| Starting Credits | Player starting money for the game. |
| Hand Buy-In | Cost to join or play a hand. |
| Player Table Name | Display or variable name for the table. |
| Create Table Prop | Spawns a table prop if one is not already placed. |
| Interaction Radius | Distance at which players can interact with the table. |

## Convoy

`SFA_Module_Convoy` spawns and routes a vehicle convoy. It is useful for ambushes, escort missions, patrol traffic, supply runs, and reinforcements.

How it works:

- The module creates vehicles, crews, and escorts for the selected side.
- It routes the convoy toward an end marker or fallback route.
- It can create route markers and spawn reinforcement waves when the convoy is attacked.

What can be changed:

| Attribute group | What it changes |
| --- | --- |
| End Marker / fallback | Destination marker or fallback distance and bearing when no marker is used. |
| Convoy Side | BLUFOR, OPFOR, INDFOR, or another configured side behavior. |
| Vehicle Classes / Vehicle Count | Which vehicles spawn and how many. |
| Crew and Escort Classes | Which unit classes crew and protect the convoy. |
| Escorts Per Vehicle | How many escorts are assigned per convoy vehicle. |
| Route Mode / Spacing / Completion Radius | How waypoints are generated and considered complete. |
| Behaviour / Speed | AI movement posture and convoy travel speed. |
| Reinforcement settings | Whether reinforcements spawn, how many waves, groups, group size, vehicles, delay, cooldown, and spawn distance. |
| Create Route Markers | Adds visible markers for the generated route. |

## Occupation Zone

`SFA_Module_Occupation` populates a zone with a military presence. It can create patrols, garrisons, vehicles, static weapons, checkpoints, and reinforcements.

How it works:

- The module uses a radius around its placed position as the occupied area.
- It spawns units for the selected side using configured class lists.
- It can create a zone marker and optionally reinforce the zone after contact.

What can be changed:

| Attribute group | What it changes |
| --- | --- |
| Zone Radius | Size of the occupied area. |
| Occupying Side | Which side owns the zone. |
| Infantry Classes | Unit classnames used for patrol and garrison spawns. |
| Patrol Groups / Patrol Size | Number and size of patrol groups. |
| Garrison Units | Number of static defensive infantry. |
| Vehicle Classes / Vehicles | Vehicles placed in the zone. |
| Static Weapon Classes / Static Weapons | Turrets or static guns placed in the zone. |
| Checkpoints / Checkpoint Props | Roadblock or checkpoint composition behavior. |
| Reinforcement settings | Waves, groups, group size, vehicle classes, vehicle count, aircraft classes, aircraft count, delay, cooldown, and spawn distance. |
| Create Zone Marker | Adds a marker showing the occupied area. |

## Trap / Alarm Inventory

`SFA_Module_InventoryTrap` makes a container dangerous or monitored. Use it for trapped loot, theft alarms, base security, evidence lockers, and scripted mission consequences.

How it works:

- The module watches for inventory access or loot behavior.
- It can notify nearby units, set mission variables, run server code, damage the container, or trigger an explosion ammo class.
- Cooldowns and execute-once behavior control whether it can fire multiple times.

What can be changed:

| Attribute | What it changes |
| --- | --- |
| Activate When | Condition that triggers the trap or alarm. |
| Execute Once Per Container | Prevents the same container from firing repeatedly. |
| Repeat Cooldown | Delay before the trap can trigger again. |
| Alarm Recipients | Who receives the alarm message. |
| Alarm Radius | Area affected by the alarm. |
| Alarm Message | Text sent when the alarm fires. |
| Alarm Sound Class | Sound played with the alarm. |
| Set Variable Name | Mission variable set by the trap. |
| Trigger Variable Name | Variable used to trigger other mission logic. |
| Server Code | Code executed on the server when the trap fires. |
| Container Damage | Damage applied to the container. |
| Explosion Ammo Class | Ammo classname used for explosion behavior. |
