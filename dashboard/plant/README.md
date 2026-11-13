# Plant

<img width="800" alt="A plant card with its soil moisture and conductivity, in light and dark mode" src="https://raw.githubusercontent.com/hazymorning/origami/main/images/v3/plant.webp">

A plant's status, soil moisture and conductivity in one row. A tap opens the plant.

## Requirements

- [Get started](../../README.md#get-started), with the Base module
- A plant entity with `problem`, `moisture` and `conductivity` attributes, as
  provided by the plant integration used for this card

## Setup

1. In [`card.yaml`](card.yaml), replace every occurrence of `plant.houseplant`
   with the plant's entity ID, including those in the templates and styles.
2. Change the fallback name `Plant` and the status texts if needed.
3. Add [`card.yaml`](card.yaml) to the dashboard. For more plants, copy the card
   and change every entity reference in the copy.

The plant entity supplies the problem state and its thresholds. If it uses
different attributes or problem strings, adapt the templates to the integration.

## Entities

| Entity | Used for |
| --- | --- |
| `plant.houseplant` | Name, status, measurements and more-info dialog |
