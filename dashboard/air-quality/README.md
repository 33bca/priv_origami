# Air quality

<img width="800" alt="An air quality card with PM2.5 and VOC, in light and dark mode" src="https://raw.githubusercontent.com/hazymorning/origami/main/images/v3/air-quality.webp">

PM2.5 and VOC in one row, with a status for the air quality. A tap opens the sensor.

## Requirements

- [Get started](../../README.md#get-started), with the Base module
- A sensor whose state is PM2.5 in µg/m³ and whose `voc_index` attribute
  contains its VOC index

## Setup

1. In [`card.yaml`](card.yaml), replace every occurrence of
   `sensor.living_room_pm25` with the sensor's entity ID, including those in
   the templates and styles.
2. Adjust the status texts and the thresholds if needed.
3. Add [`card.yaml`](card.yaml) to the dashboard.

PM2.5 values above 12 are marked as moderate and values above 35 as poor.
The VOC reading is colored at values above 150 and above 300. These are the
card's display thresholds, not a medical assessment.

## Entities

| Entity | Used for |
| --- | --- |
| `sensor.living_room_pm25` | PM2.5, VOC index, status and more-info dialog |
