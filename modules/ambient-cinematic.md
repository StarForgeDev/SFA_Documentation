---
title: Ambient and Cinematic Modules
---

# Ambient and Cinematic Modules

These modules help build atmosphere around scenes without writing mission scripts from scratch.

## Ambient Civilian

Class: `SFA_Module_AmbientCivilian`

Function: `SFA_fnc_moduleAmbientCivilian`

The Ambient Civilian module manages pedestrians, traffic, police, and cleanup behavior around an area.

Important settings include:

- `SFA_AmbientCivilian_EnablePedestrians`
- `SFA_AmbientCivilian_EnableTraffic`
- `SFA_AmbientCivilian_MaxPedestrians`
- `SFA_AmbientCivilian_MaxVehicles`
- `SFA_AmbientCivilian_EnablePolice`
- `SFA_AmbientCivilian_MaxPolice`

Use it for towns, ports, city streets, market scenes, and other non-combat areas. Test performance before using high civilian and vehicle counts.

## Intro Text

Class: `SFA_Module_IntroText`

Function: `SFA_fnc_moduleIntroText`

The Intro Text module displays title, subtitle, and optional additional text with configurable font, color, timing, fade, and sound.

Common fields:

- `SFA_IntroText_Title`
- `SFA_IntroText_Subtitle`
- `SFA_IntroText_AdditionalLine`
- `SFA_IntroText_FadeIn`
- `SFA_IntroText_Duration`
- `SFA_IntroText_FadeOut`
- `SFA_IntroText_Sound`

## Cinematic Border

Class: `SFA_Module_CinematicBorder`

Function: `SFA_fnc_moduleCinematicBorder`

The Cinematic Border module adds letterbox bars and optional title/subtitle text.

Common fields:

- `SFA_CinematicBorder_BarSize`
- `SFA_CinematicBorder_Fade`
- `SFA_CinematicBorder_Duration`
- `SFA_CinematicBorder_Title`
- `SFA_CinematicBorder_Subtitle`
- `SFA_CinematicBorder_TitleSize`
- `SFA_CinematicBorder_SubtitleSize`
- `SFA_CinematicBorder_TextY`

## Test Status

Verify display scaling on different UI sizes and resolutions. Multiplayer behavior should be tested for local versus global display timing.
