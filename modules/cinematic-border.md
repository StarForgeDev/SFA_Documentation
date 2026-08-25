---
title: Cinematic Border
---

# Cinematic Border

Class: `SFA_Module_CinematicBorder`

Function: `SFA_fnc_moduleCinematicBorder`

[Back to Modules](../)

## What It Is

Cinematic Border adds letterbox bars and optional title/subtitle text. It is a presentation module for cutscenes, dialogue, dramatic reveals, mission endings, landing scenes, and scripted story moments.

Use it when you want a scene to feel intentionally cinematic without building a full custom UI.

## How It Works

The module displays a screen overlay with top and bottom bars. It can fade the bars in, keep them visible for a duration, and fade them out. Optional text can be shown while the border is active.

The border is visual only. It does not automatically disable player controls, force camera movement, pause AI, or hide the rest of the UI unless the mission handles those separately.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Show Border | Enables or disables the letterbox bars. |
| Border Size | Controls how tall the bars are. Larger bars feel more cinematic but cover more screen space. |
| Fade Time | Controls how quickly the bars appear or disappear. |
| Duration | How long the effect stays active. |
| Title | Main text displayed with the border. |
| Subtitle | Secondary text displayed with the border. |
| Title Size | Size of the title text. |
| Subtitle Size | Size of the subtitle text. |
| Text Vertical Position | Moves the title/subtitle vertically on the screen. |

## Mission-Maker Notes

- Pair it with scripted camera work, dialogue, or intro text for stronger presentation.
- Keep border duration short if players still have control.
- Do not place critical UI elements under the covered screen area.

## Testing

Check UI scale, resolution differences, fade timing, and multiplayer timing. If only some clients should see the cinematic, verify the trigger scope before using it in an operation.
