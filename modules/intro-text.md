---
title: Intro Text
---

# Intro Text

Class: `SFA_Module_IntroText`

Function: `SFA_fnc_moduleIntroText`

[Back to Modules](../)

## What It Is

Intro Text displays a styled mission-opening or transition title. It supports a main title, subtitle, additional line, font choices, colors, fade timing, visible duration, and optional sound.

Use it for episode titles, location cards, operation names, chapter breaks, time skips, or cinematic scene starts.

## How It Works

When triggered by the mission/module system, it sends formatted text to the player's UI. The mission maker controls the text content and presentation. Fade values define how the text enters and leaves the screen, while the visible duration controls how long players can read it.

If a sound class is provided, the intro can play an audio cue at the same time as the visual.

## What Can Be Changed

| Setting | What it does |
| --- | --- |
| Title | Main text line. Usually the operation name, planet, or chapter title. |
| Title Font | Font used by the title line. |
| Title Font Size | Size of the title. Increase for major cinematic intros; reduce for subtle location cards. |
| Title Font Color | Color of the title text. Use high contrast for readability. |
| Subtitle | Secondary text line. Usually location, time, unit, or context. |
| Subtitle Font | Font used by the subtitle. |
| Subtitle Font Size | Size of the subtitle. |
| Subtitle Font Color | Color of the subtitle text. |
| Additional Line | Optional third line for extra context. |
| Additional Font | Font used by the additional line. |
| Additional Font Size | Size of the additional line. |
| Additional Font Color | Color of the additional line. |
| Fade In Time | How long the text takes to appear. |
| Visible Duration | How long the text remains fully visible. |
| Fade Out Time | How long the text takes to disappear. |
| Sound Class | Configured sound class to play with the intro. |

## Mission-Maker Notes

- Keep text short enough that players can read it during movement.
- Use this for presentation, not objective instructions that players must remember under pressure.
- If you use a sound class, verify the sound is defined in mission or addon config.

## Testing

Check UI scale, ultrawide/small resolution behavior, text readability, and whether the sound plays for every intended client in multiplayer.
