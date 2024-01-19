---
title: Главная
description: Позволяет играть в режиме deathmatch (CSDM) в Counter-Strike 1.6 (с возможностью возрождения, выбором оружия, защитой при спавне и т. д.).
---

# 
<p align="center">
    <a href="https://github.com/wopox1337/ReDeathmatch">
        <img
            width="500px"
            alt="Логотип с оружием"
            src="https://user-images.githubusercontent.com/18553678/233882657-0ee4d8ea-2492-4af7-8db5-32430689c131.png"
        >
    </a>
</p>

<p align="center">
    Плагины AMXModX для предоставления игры в режиме Deathmatch в <a href="https://store.steampowered.com/app/10/CounterStrike/">Counter-Strike 1.6</a>, оптимизированные для работы с <a href="https://github.com/s1lentq/ReGameDLL_CS">ReGameDLL_CS</a>.
</p>

<p align="center">
    <a href="https://github.com/wopox1337/ReDeathmatch/releases/latest">
        <img
            src="https://img.shields.io/github/downloads/wopox1337/ReDeathmatch/total?label=Скачать@Последний%20релиз&style=flat-square&logo=github&logoColor=white"
            alt="Статус сборки"
        >
    </a>
    <a href="https://github.com/wopox1337/ReDeathmatch/actions">
        <img
            src="https://img.shields.io/github/actions/workflow/status/wopox1337/ReDeathmatch/CI.yml?branch=master&style=flat-square&logo=github&logoColor=white"
            alt="Статус сборки"
        >
    </a>
    <a href="https://github.com/wopox1337/ReDeathmatch/releases">
        <img
            src="https://img.shields.io/github/v/release/wopox1337/ReDeathmatch?include_prereleases&style=flat-square&logo=github&logoColor=white"
            alt="Релиз"
        >
    </a>
    <a href="https://www.amxmodx.org/downloads-new.php">
        <img
            src="https://img.shields.io/badge/AMXModX-1.9 | 1.10-blue?style=flat-square"
            alt="Зависимость от AMXModX"
        ></a>
    <a href="https://discord.gg/fC2AasCPfh">
        <img src="https://img.shields.io/discord/1099870919138213890?style=flat-square&logo=discord&label=Discord%20&labelColor=%237289DA" alt="Discord Shield"
        ></a>
</p>

## О моде
Мод является полностью переписанной реализацией [CSDM ReAPI](https://github.com/wopox1337/CSDM-ReAPI) для замены устаревшего кода.

Мод основан на успешном опыте [CSDM 2.1.2 от BAILOPAN](https://www.bailopan.net/csdm), но использует современные возможности нового [ReGameDLL_CS](https://github.com/s1lentq/ReGameDLL_CS).

Множество функций уже давно встроено и оптимизировано для работы непосредственно в ReGameDLL_CS, мод теперь только переключает настройки игры и предоставляет удобный способ управления.

## Особенности
- Сохранение настроек игры (CVars);
- Режимы раунда (*НОВОЕ*);
- Динамическая перезагрузка конфигурации;
- Случайные точки спавна и предустановки (можно добавлять новые точки спавна и предустановки);
- Защита при спавне (настраиваемая по времени и отображению игрока);
- Интерактивный редактор спавна;
- Настраиваемые меню оружия;
- Командная смерть, а также свободный для всех режим (FFA Deathmatch);
- Большие фрагменты оптимизированы в ReGameDLL_CS;
- Поддержка многоязычности;
- Поддержка дополнительных конфигураций:
    - Для отдельной карты (`redm/extraconfigs/de_dust2.json`);
    - Для префикса карты (`redm/extraconfigs/prefix_aim.json`).
- Нативная поддержка Counter-Strike: Condition Zero;
- Поддержка группировки точек спавна;
- Возможность использовать мод в качестве основы для разработки других режимов (например, `GunGame`).
