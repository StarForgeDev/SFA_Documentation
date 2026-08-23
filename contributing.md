---
title: Contributing
---

# Contributing to the Docs

This documentation should stay practical and testable.

## Writing Style

- Use short sections.
- Prefer exact classnames over vague names.
- Include the source folder when relevant.
- Mark untested behavior clearly.
- Do not claim multiplayer behavior is confirmed unless it was tested in multiplayer.

## Page Template

Use this structure for new module pages:

```markdown
# Module Name

Class: `SFA_Module_Name`

Function: `SFA_fnc_moduleName`

Short purpose paragraph.

## Basic Setup

1. Place the module.
2. Sync required objects.
3. Configure required fields.
4. Test in mission.

## Settings

| Setting | Property | Use |
| --- | --- | --- |

## Multiplayer Notes

## Example Setup

## Test Status
```

## Runtime Evidence

Use clear labels:

- `Source verified` means the config or script contains the documented field.
- `Packed PBO verified` means the addon packed without errors and loaded.
- `Singleplayer verified` means tested in a local mission.
- `Hosted MP verified` means tested in hosted multiplayer.
- `Dedicated verified` means tested on a dedicated server.
- `JIP verified` means join-in-progress behavior was tested.
