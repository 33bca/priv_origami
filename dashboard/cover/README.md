# Cover

<img width="800" alt="A cover card with open and close keys and an optional preset key, in light and dark mode" src="https://raw.githubusercontent.com/hazymorning/origami/next/images/v3/cover.webp">

A cover's state and position, with keys to open and close. A cover that supports tilt also gets a preset key.

## Requirements

- [Get started](../../README.md#get-started), with the modules Base and Cover
- A cover entity that supports position

## Setup

1. In [`card.yaml`](card.yaml), replace `cover.living_room_blind` with the cover's entity ID.
2. Add [`card.yaml`](card.yaml) to the dashboard, as described under [Get started](../../README.md#get-started).

## Optional

- The preset key appears only when the cover supports tilt. To use it, create `script.cover_preset` from [`preset.yaml`](preset.yaml), then set its position and tilt targets in [`card.yaml`](card.yaml). Remove the middle sub-button from `card.yaml` to leave the key out.

## Entities

| Entity | Used for |
| --- | --- |
| `cover.living_room_blind` | The cover, its state and position, and the open and close keys |
| `script.cover_preset` | Sets the cover's position and tilt for the optional preset key |
