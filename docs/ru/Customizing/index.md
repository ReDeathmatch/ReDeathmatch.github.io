## Основная конфигурация
Находится в файле `amxmodx/configs/redm/gamemode_deathmatch.json`.

???+ note
    Все, что относится к режиму Deathmatch, **должно** быть настроено только в этом файле.

## Дополнительная конфигурация:
Поддерживается дополнительная конфигурация путем загрузки конфигурации для:

  - Определенной карты (`configs/redm/extraconfigs/<название_карты>.json`);
  - Префикса карты (`configs/redm/extraconfigs/prefix_<префикс_карты>.json`);

Порядок поиска файла с настройками для загрузки:

  - Поиск файла конфигурации для карты;
  - Поиск файла конфигурации для префикса карты;
  - Поиск основного файла конфигурации (`configs/redm/gamemode_deathmatch.json`).

Найденный и использованный файл конфигурации сопровождается информационным сообщением в консоли сервера:
```js
[1.00][INFO] FindConfigFile: Config `gamemode_deathmatch.json` loaded.
```

Если ни один из файлов конфигурации не будет найден, плагин выдаст ошибку:
```json
FindConfigFile: Can't find any config file!
```

Каждый файл конфигурации, который требуется загрузить, **должен** иметь действительную схему JSON!

## Структура файла конфигурации
Файл конфигурации состоит из разделов:

 - equip
    - primary - Основное оружие (штурмовые винтовки, снайперские винтовки);
    - secondary - Вторичное оружие (пистолеты и пулеметы);
 - cvars - CVars для изменения игрового процесса при включении режима Deathmatch;
 - modes - Список режимов раундов.

## Раздел `equip`
### Primary
Список оружия, которое используется для оснащения игрока в слотах основного оружия (штурмовые винтовки, снайперские винтовки, ПП и т. д.).

### Secondary
Список оружия, чтобы оснастить игрока в слоте вторичного оружия (пистолеты).

## Раздел `cvars`
Список CVars сервера для изменения геймплея при включении режима Deathmatch. Каждый CVar из этого списка восстанавливает свое исходное значение при отключении режима Deathmatch (система запоминает исходное значение CVar перед его изменением).

## Раздел `modes`
Это необязательный раздел.
Содержит список конфигураций режимов для раундов (Multi-CFG), фактически содержит полную структуру для описанной выше конфигурации.
Исключение составляют параметры:

 - `name` - Название режима.

    Отображается игрокам при возрождении, переключении режимов.

    Может содержать ключ LANG, определенный в файле `amxmodx\data\lang\redm\modes.txt`, если ключ LANG будет найден в предоставленном словаре.