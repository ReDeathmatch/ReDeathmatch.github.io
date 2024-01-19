The basic set of plugins necessary for Deathmatch mode is defined in the file `amxmodx\configs\plugins-redm.ini`:

## Structure
```ini
; Main plugin
ReDeathmatch.amxx debug ; Main mod

; Addons
redm_spawns.amxx debug ; System for working with spawn points (player revives, items (TODO))
```

The order of the plugins is important for loading, not recommended for modding!