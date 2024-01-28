Для правильной работы системы и ее функций необходимо установить следующее:

- Установить [сервер HLDS](https://developer.valvesoftware.com/wiki/Half-Life_Dedicated_Server);
- Установить [ReGameDLL_CS](https://github.com/s1lentq/ReGameDLL_CS);
- Установить AMXModX ([v1.9](https://www.amxmodx.org/downloads-new.php) или [v1.10](https://www.amxmodx.org/downloads-new.php?branch=master));
- Установить модуль [ReAPI](https://github.com/s1lentq/reapi) для AMXX.

## Проверьте установленные компоненты:
???+ note
    Приведённые версии компонентов не являются требованием, рассмаотриваются как пример вывода информации.

### Версия HLDS

с помощью команды: `version`
```js
] version

Protocol version 48
Exe version 1.1.2.7/Stdio (cstrike)
ReHLDS version: 3.13.0.783-dev
Build date: 00:06:04 Feb 11 2023 (3227)
Build from: https://github.com/dreamstalker/rehlds/commit/1796459
```

### Версия ReGameDLL

с помощью команды: `game version`
```js
] game version

Версия ReGameDLL: 5.22.0.594-dev
Дата сборки: 22:19:38 Apr 03 2023
Собрано из: https://github.com/wopox1337/ReGameDLL_CS/commit/71e61e6
```

### Версия AMXModX

просмотр списка загруженных модулей: `meta list`
```js
] meta list

Currently loaded plugins:
      description   stat pend  file                  vers             src  load  unload
 [ 1] AMX Mod X     RUN   -    amxmodx_mm.dll        v1.10.0.5467     ini  Start ANY
 [ 2] Ham Sandwich  RUN   -    hamsandwich_amxx.dll  v1.10.0.5467     pl1  ANY   ANY
 [ 3] FakeMeta      RUN   -    fakemeta_amxx.dll     v1.10.0.5467     pl1  ANY   ANY
 [ 4] ReAPI         RUN   -    reapi_amxx.dll        v5.23.0.263-dev  pl1  ANY   Never
4 plugins, 4 running
```

### Версия ReAPI

просмотр списка модулей AMXX: `amxx modules`
```js
] amxx modules

Currently loaded modules:
      name                    version     author               status
 [ 1] Ham Sandwich            1.10.0.546  AMX Mod X Dev Team   running
 [ 2] FakeMeta                1.10.0.546  AMX Mod X Dev Team   running
 [ 3] JSON                    1.10.0.546  AMX Mod X Dev Team   running
 [ 4] ReAPI                   5.23.0.263  Asmodai & s1lent     running
4 modules, 4 correct
```
