### Old format

Mods that inherit the old configuration system:

- CSDM by BAILOPAN
- ReCSDM by ReHLDS Team
- CSDM-ReAPI by Vaqtincha
- CSDM-ReAPI by wopox1337

Location of spawn configuration files:
```cpp
amxmodx/
└── configs/
    └── csdm/
        └── spawns/
            └── *.spawns.cfg
```

The old respawn system has the following format:
```cpp title="de_dust.spawns.cfg"
-723    487     51  4   -35     0   0   -1  -35 0
363     457     51  5   -126    0   0   -2  -126 0
742     -341    51  3   131     0   0   -1  131 0
...
```

Description of parameters:

| origin X | origin Y | origin Z | angle X | angle Y | angle Z | team | viewAngle X | viewAngle Y | viewAngle z |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| -2198 | -538 | 179 | 8 | -34 | 0 | 0 | -3 | -34 | 0 |

Some old formats may only have the following parameters:

- Origin X, Origin Y, Origin Z
- Angle X, Angle Y, Angle Z

Drawbacks of the old format:

- Insufficient data precision;
- Inability to extend the format while maintaining backward compatibility;
- Difficulty in manually adjusting parameters due to undocumented format;
- Presence of unnecessary parameters that do not affect gameplay (Z-axis);
- Limitation on respawn points.

Compilation of old spawns:

- [AlliedMods topic](https://forums.alliedmods.net/showthread.php?t=49537)

### New format

Location of spawn configuration files:
```js
amxmodx/
└── data/
    └── redm/
        └── *.spawns.json
```

The configuration of ReDeathmatch respawn files is different and uses the `JSON5` data format:
```json title="de_dust2.spawns.json"
{
    "spawns": [
        {
            "team": 0,
            "group": "a",
            "origin": [
                -879.96875,
                -1007.96875,
                192.01966857910156
            ],
            "angle": [
                -1.5692138671875,
                42.60498046875
            ],
            "vAngle": [
                4.7076416015625,
                42.60498046875
            ]
        },
        ...
    ]
}
```

The new format of configuration has advantages over the old system:

- Ability to extend the configuration without losing backward compatibility;
- Following the widely accepted `JSON5` standard for ease of use even outside ReDeathmatch;
- High precision float data.

The new format of configuration is necessary considering the advantages of the new format and the drawbacks of the old one. The insufficient precision of the old format prevented adding spawn points in "tight" areas, where there might be a need to place the player in a sitting position or close to other objects.