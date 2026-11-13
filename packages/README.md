# Fabian's Origami packages

These are the helpers and scripts for Fabian's dashboard. The files are Home
Assistant packages, not standalone script files. Use the complete set with
[`dashboard-fabian.yaml`](../dashboard/dashboard-fabian.yaml).

## Installation

1. Back up the current configuration.
2. Copy the `origami-*.yaml` files in this folder to `/config/packages/`.
3. If migrating from the former `origami-fabian.yaml`, remove that old file
   from `/config/packages/`. Do not load it alongside the new files, or the
   same helpers and scripts will be defined twice.
   If `origami-room-off.yaml` or `origami-now-playing.yaml` was previously
   copied there, remove those files too.
4. Ensure `configuration.yaml` loads the directory:

   ```yaml
   homeassistant:
     packages: !include_dir_named packages
   ```

5. Check the configuration in Home Assistant and restart it.

The retained helper unique IDs and script IDs stay the same. Check other
dashboards and automations before removing the old package, especially if
they use removed helpers or scripts such as `input_boolean.all_rooms`,
`script.room_off`, `sensor.active_target` or `sensor.active_speaker`.

## Files and updates

| Package | Contents | V3 reference |
| --- | --- | --- |
| `origami-rooms.yaml` | Climate-table toggle | [Rooms](../dashboard/rooms/README.md) |
| `origami-music.yaml` | Selected speaker and group-volume helper | [Music](../dashboard/music/README.md) |
| `origami-playback.yaml` | Playback script | [Playback](../dashboard/music/playback.yaml) |
| `origami-set-group-volume.yaml` | Group-volume script | [Set group volume](../dashboard/music/set-group-volume.yaml) |
| `origami-group-speakers.yaml` | Speaker-grouping script | [Group speakers](../dashboard/music/group-speakers.yaml) |
| `origami-volume.yaml` | TV volume-step script | [Volume](../dashboard/tv/volume.yaml) |
| `origami-thermostat-step.yaml` | Thermostat-step script | [Thermostat step](../dashboard/room/thermostat-step.yaml) |
| `origami-cover-preset.yaml` | Cover-preset script | [Cover preset](../dashboard/cover/preset.yaml) |

When updating a script, compare it with its V3 reference and retain its package
wrapper, script ID and any personal settings.
