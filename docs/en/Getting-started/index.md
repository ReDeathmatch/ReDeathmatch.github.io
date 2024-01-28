# Getting started

ReDeathmatch is a AMXModX plugins to provide Deathmatch gameplay in <a href="https://store.steampowered.com/app/10/CounterStrike/">Counter-Strike 1.6</a> optimized to work with <a href="https://github.com/s1lentq/ReGameDLL_CS">ReGameDLL_CS</a>.

The mod is a completely rewritten implementation of [CSDM ReAPI](https://github.com/wopox1337/CSDM-ReAPI), to replace legacy code.

Mod made a look back on the successful experience [CSDM 2.1.2 by BAILOPAN](https://www.bailopan.net/csdm), but using modern features of the new [ReGameDLL_CS](https://github.com/s1lentq/ReGameDLL_CS).

A variety of functions have long been built-in and optimized to work directly in ReGameDLL_CS. The ReDeathmatch system mostly just switches game settings and provides a convenient way to control most of the functionality.

## Project architecture

```markdown
amxmodx/
├── configs/
│   ├── redm/
│   │   ├── extraconfigs/ - additional configurations (optional)
│   │   │   ├── <mapname>.json - configuration activated on a specific map
│   │   │   └── prefix_<mapPrefix>.json - configuration activated for maps with a certain prefix
│   │   └── gamemode_deathmatch.json - main configuration file for the mod
│   └── plugins-redm.ini - activation of ReDeathmatch in AMXModX
├── data/
│   ├── lang/
│   │   └── redm/
│   │       ├── modes.txt - multilingualism for DM modes
│   │       └── redm.txt - multilingualism for ReDM
│   └── redm/ - respawn file configuration
│       └── *.spawns.json
├── plugins/ - compiled files for mod activation
│   ├── ReDeathmatch.amxx - main mod
│   └── redm_spawns.amxx - editor/handler for respawn points
└── scripting/ - mod source code
    ├── include/
    │   ├── msgstocks.inc
    │   ├── redm_version.inc
    │   └── redm.inc
    ├── ReDeathmatch/
    │   └── **/*.sma
    ├── ReDeathmatch.sma
    └── redm_spawns.sma
```