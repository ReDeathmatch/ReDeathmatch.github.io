### Description of the Process

1) When entering `redm_convert_spawns`, the system searches for the folder `/amxmodx/configs/csdm/spawns`.

2) It looks for files with the mask `<map_name>.spawns.cfg` and opens each file for conversion.

3) By opening each file, the system reads the spawn configuration line by line, following the format described above in the old system. Each line should have **10 parameters**, and invalid lines will be skipped.

4) While reading each line, an object is formed with the converted parameters corresponding to the new system.

5) After reading all the lines, the generated array of objects is written to the file `data/redm/converted/<map_name>.spawns.json`. The map name is taken from the name of the old spawn configuration file.

Successful conversion is confirmed by an informational message in the server console:
```js
Editor_ConvertSpawns: Successfully convert `15` old spawn files.
```
???+ note
    During the conversion process, errors or warnings may occur (unable to open file for reading/writing, unable to create a folder, etc.), which will be explicitly reflected in the server console and log files.

### Using the Converted Files
To use the converted respawn configurations, **it is necessary to move** all the files from `data/redm/converted/<map_name>.spawns.json` to `data/redm/<map_name>.spawns.json`.

The converted respawn configurations placed in the directory described above can then be edited using the built-in ReDeathmatch system using the command `redm_edit_spawns`.