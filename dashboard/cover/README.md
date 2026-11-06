# Cover

<img width="800" alt="A cover card with open, tilt and close controls, in light and dark mode" src="https://raw.githubusercontent.com/hazymorning/origami/next/images/v3/cover.webp">

A cover's state and position, with keys to open, tilt and close it.

## Requirements

- [Get started](../../README.md#get-started), with the modules Base and Cover
- A cover entity that supports position and tilt

## Setup

1. Open [Scripts](https://my.home-assistant.io/redirect/scripts/) and select **Create script**, then **Create new script**.
2. In the three-dot menu, select **Edit in YAML**, paste [`preset.yaml`](preset.yaml) and save it as **Cover preset**, so its entity ID is `script.cover_preset`.
3. In [`card.yaml`](card.yaml), replace `cover.living_room_blind` with the cover's entity ID and set the target position and tilt for the middle key.
4. Add [`card.yaml`](card.yaml) to the dashboard, as described under [Get started](../../README.md#get-started).

## Entities

| Entity | Used for |
| --- | --- |
| `cover.living_room_blind` | The cover, its state and position, and the open, tilt and close keys |
| `script.cover_preset` | Sets the cover's position and tilt for the middle key |
