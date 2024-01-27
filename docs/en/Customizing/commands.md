## Admin commands
| Name |  Description | Access level | Plugin |
| ------------ | --------------- | ------ | -------- |
| redm_status          | Notifies in console about the status of the mod                                | f   | ReDeathmatch |
| redm_disable         | Disables the Deathmatch system                                                  | f   | ReDeathmatch |
| redm_enable          | Enables the Deathmatch system                                                   | f   | ReDeathmatch |
| redm_reload          | Restarts the Deathmatch system                                                  | f   | ReDeathmatch |
| redm_dump_cvars      | Displays in console a list of the CVars loaded by the system                               | f   | ReDeathmatch |
| redm_dump_equip      | Displays in console a list of loaded ammunition, currently available to players            | f   | ReDeathmatch |
| redm_convert_spawns  | Converts old spawn files for the new system                                     | f   | redm_spawns |
| redm_edit_spawns     | Toggles the spawn editing mode                                                  | f   | redm_spawns |

### Using `redm_reload`
Arguments:

 - `<file_name>` - the name of the config file (optional)

The system reads the [[config file|Configuration]], resets the current round mode (if enabled), and notifies the console of a successful reboot.
> If the command argument is used, it will search for this file in the `amxmodx/configs/redm/<file_name>` folder.

Example: `redm_reload custom_config.json`

### Using `redm_convert_spawns`
When using the command, the system looks for files with the mask `<map_name>.spawns.cfg` in the directory `amxmodx/configs/csdm/spawns/`.
During recursive traversal (checking) of the folder, every found file that matches the mask (format) will be read and transformed into a new architecture (JSON format).
The new, converted files will be located in the folder `amxmodx/data/redm/converted/` and have a mask like: `<map_name>.spawns.json`.

After a successful conversion, the system will let you know that the conversion was successful:
`Editor_ConvertSpawns: Succefully convert N old spawn files.`

In case of any errors during the work of the converter, the system will inform in the server console (as well as in the logs) the reasons of operability.

---

## Public commands
| Name | Description | Plugin |
| ------------ | -------- | ------ |
| redm               | Outputs in console basic information about the mod used | ReDeathmatch |
| !guns, /guns, drop | Switches the equipment selection menu        | ReDeathmatch |
