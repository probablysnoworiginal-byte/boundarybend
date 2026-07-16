---
aliases:
  - BoundaryBend Art Style
  - Visual Bible
tags:
  - boundarybend/project
  - boundarybend/art-direction
status: established
cssclasses:
  - visual-direction
---

# Visual Direction

> [!bb-hero]
> # SUN-BAKED, FACETED, ALIVE
> ### BoundaryBend should feel shaped by broad planes, stepped light, and storybook color—not surface noise.

This is the visual contract shared by reference work, environment planning, and production assets.

## Default asset contract

- **Geometry carries silhouette and facets.** Form comes from the model, not painted shading.
- Base colors contain **no painted highlights or shadows**.
- Ordinary world assets use the project’s low-poly band-lit material family.
- Smoothness, normal maps, and transparency are absent by default.
- A hard highlight belongs only on materials that genuinely need to read as metal.
- VFX remains a separate unlit family.
- Static props do not gain armatures, scripts, animation, or extra hierarchy without a reason.

## The four global looks

| Look | Visual behavior | Best use |
|---|---|---|
| **Sun-Baked Storybook** | Three light bands, warm ivory filter, slate-violet shadows, gentle fog | Neutral world, deep history, humane daylight |
| **Dry Heat** | Three bands, copper filter, wine-red shadows, restrained saturation | Pressure, transition, exposed danger, the last century |
| **Blue Moon** | Two bands, cold blue filter, deep navy fog, modest bloom | Graphic night, secrecy, isolation, the present Ossuary boundary |
| **Dream Cartridge** | Four bands, violet shadows, stronger separation and bloom | Deliberately unreal spaces—not the everyday default |

## Temporal color grammar

| Distant past | Last century | Present |
|---|---|---|
| Sun-Baked Storybook | Dry Heat | Blue Moon |
The art direction stays constant while lighting carries temporal meaning. This is a useful grammar, not a universal law: the distant past need not always be warm, and the present need not always be blue.

## Performance guardrail

Pixelation, palette quantization, dithering, and outlines are not assumed screen-wide features. They should become full-screen treatments only if profiling shows that the visual return earns the cost.

## Production relationship

The working look laboratory remains the implementation reference. This page states the public-facing creative contract behind its shaders, materials, presets, and scenes.
