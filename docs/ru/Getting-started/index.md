**ReDeathmatch** - это плагины **AMXModX**, предоставляющие геймплей _Deathmatch_ в [Counter-Strike 1.6](https://store.steampowered.com/app/10/CounterStrike/), оптимизированные для работы с [**ReGameDLL_CS**](https://github.com/s1lentq/ReGameDLL_CS).

Мод является полностью переписанной реализацией [CSDM ReAPI](https://github.com/wopox1337/CSDM-ReAPI) и заменяет устаревший код.

Мод основан на успешном опыте [CSDM 2.1.2 от BAILOPAN](https://www.bailopan.net/csdm), но использует современные возможности нового [ReGameDLL_CS](https://github.com/s1lentq/ReGameDLL_CS).

Множество функций уже давно встроено и оптимизировано для работы непосредственно в ReGameDLL_CS, система ReDeathmatch по большей части только переключает настройки игры и предоставляет удобный способ управления большинством функциональности.

## Архитектура проекта
```
amxmodx/
├── configs/
│   ├── redm/
│   │   ├── extraconfigs/ - дополнительные конфигурации (опционально)
│   │   │   ├── <mapname>.json - конфигурация активирующаяся на определённой карте
│   │   │   └── prefix_<mapPrefix>.json - конфигурация активирующаяся для карт с определённым префиксом
│   │   └── gamemode_deathmatch.json - главный файл конфигурации мода
│   └── plugins-redm.ini - активация ReDeathmatch в AMXModX
├── data/
│   ├── lang/
│   │   └── redm/
│   │       ├── modes.txt - мультиязычность для режимов DM
│   │       └── redm.txt - мультиязычность ReDM
│   └── redm/ - конфигурация respawn-файлов
│       └── *.spawns.json
├── plugins/ - скомпилированные файлы для активации мода
│   ├── ReDeathmatch.amxx - основной мод
│   └── redm_spawns.amxx - редактор/обработчик respawn-точек
└── scripting/ - исходный код мода
    ├── include/
    │   ├── msgstocks.inc
    │   ├── redm_version.inc
    │   └── redm.inc
    ├── ReDeathmatch/
    │   └── **/*.sma
    ├── ReDeathmatch.sma
    └── redm_spawns.sma
```