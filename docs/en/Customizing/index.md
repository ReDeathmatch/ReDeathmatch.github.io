## Main configuration 
Found in `amxmodx/configs/redm/gamemode_deathmatch.json` file.

???+ note
    Everything that relates to Deathmatch mode **must** be configured only in this file.

## Additional configuration:
There is support for additional configuration, by loading the configuration for:

  - Defined map (`configs/redm/extraconfigs/<map_name>.json` file);
  - Map prefix (`configs/redm/extraconfigs/prefix_<prefix_map>.json` file);

The order of finding a config file to load:

  - The map config is searched for;
  - The config file for the map prefix is searched;
  - The main config file is searched (`configs/redm/gamemode_deathmatch.json`).

Found and used config is accompanied by an information message in the server console:
```js
[1.00][INFO] FindConfigFile: Config `gamemode_deathmatch.json` loaded.
```

If none of the configuration files are found, the plugin will give an error:
```json
FindConfigFile: Can't find any config file!
```

Every config file to be loaded **must** have a valid JSON schema!

## Config file structure
The config file consists of sections:

 - equip
    - primary - Primary weapons (assault rifles, snipers, simi-pistols);
    - secondary - Secondary weapons (pistols);
 - cvars - CVars to be changed when turning on Deathmatch mode;
 - modes - The list of rounds modes.

## Section `equip`
### Primary.
The list of weapons which are used to equip the player in the Primary slots (assault rifles, sniper rifles, SMG, etc.).

### Secondary
The list of weapons, to equip the player in the Secondary (pistols) slot.

## Section `cvars`
A list of the CVars of the server for changing the gameplay when turning on Deathmatch mode. Each CVar in this list restores its original value when Deathmatch mode is turned off (the system remembers the original CVar value before changing it).

## Section `modes`
It is an optional section.
Contains a list of mode configurations for rounds (Multi-CFG), contains in fact a complete structure for the configuration described above.
The exceptions are the parameters:

 - `name` - Name of the mode.

    Displayed to players when reviving, switching modes.

    Can contain LANG-key defined in `amxmodx\data\lang\redm\modes.txt`, if LANG-key will be found in provided dictionary.