The mod adds new ConVars, for easy configuration.
The complete and up-to-date list can be seen with the command:
```
amxx cvars ReDeathmatch; amxx cvars redm_
```
---
| Name | Description | Value | Plugin |
| - | - | - | - |
| redm_version | **System**, displays in Source Query information about the used mod | `<version_mod>` | ReDeathmatch |
| redm_healer | HP amount given to the player (bonus) when killing an opponent | `0...maxHealth` | ReDeathmatch |
| redm_healer_hs | Amount of HP given to the player (bonus) when killing an opponent in the head | `0...maxHealth` | ReDeathmatch |
| redm_sounds_distance | Minimal distance (units) of the player from others, at which he will hear shots, steps, etc. Used to reduce noise, improve gameplay experience. | 0 - disabled or distance in `int` |ReDeathmatch |
| redm_fade | illuminate the screen for players when killing an opponent | `boolean` | ReDeathmatch |
| redm_refill_ammo | refill weapon ammunition when you kill an opponent | `boolean` | ReDeathmatch |
| redm_hitsound | sound indication of a hit on an opponent | | boolean | ReDeathmatch |
| mp_damage_headshot_only | Enable Only-headshot mode for all players | `boolean` | ReDeathmatch |
| redm_hide_other_deathnotice | Hiding someone else's kill/deathnotice events for players | `boolean` | ReDeathmatch |
| redm_spawn_preset | Selecting a preset for the spawn manager | `preset` - pre-installed; </br> `<preset_name>` - other implements | ReDeathmatch |
| redm_modes_switch | Selecting the mode of operation of the round mode (Multi-CFG) | `sequentially` - selection one by one; </br> `random` - random mode every round | ReDeathmatch |
| redm_keep_weapon_slot | When a player is respawn and equipped, the last used slot (weapon) is restored. | `boolean` | ReDeathmatch |
| redm_active | Displaying the working status of the mod | `boolean` | ReDeathmatch |
| mp_randomspawn | Random spawning for players | `0` - disabled; </br> `1` - all teams will spawn in random points; </br> `2` - only T; </br> `2` - only CT | redm_spawns |
| mp_randomspawn_los | Whether to check the visibility of the revived player's opponents before spawning on a point | `boolean` | redm_spawns |
| mp_randomspawn_dist | Minimum distance to enemies before spawning to a point | `int` | redm_spawns |
