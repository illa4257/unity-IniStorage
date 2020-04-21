# Work with ini files/Работа с ini файлами

* Code can be changed/Код можно изменять! :)

* Tested on Unity/Протестирован на Unity:
  - 2019.3.7f1

In Unity forum/На форуме Unity: [**https://forum.unity.com/threads/read-write-ini-file-chtenie-zapis-ini-fajla.857215/**](https://forum.unity.com/threads/read-write-ini-file-chtenie-zapis-ini-fajla.857215/)

## EN

Documentation [**here**](https://github.com/illa4257/iniStorageForUnity/blob/master/docs/en.md).

### How to put?

Move the [**script**](https://github.com/illa4257/iniStorageForUnity/releases) to the project.

### Example:
```c#
iniStorage iniParser = new iniStorage;

iniParser.path = "config.ini";
iniParser.set("test", "myValue");
Debug.Log(iniParser.get("test"));
```

## RU

Документация [**здесь**](https://github.com/illa4257/iniStorageForUnity/blob/master/docs/ru.md).

### Как поставить?

Переместите [**скрипт**](https://github.com/illa4257/iniStorageForUnity/releases) в проект.

### Пример:
```c#
iniStorage iniParser = new iniStorage;

iniParser.path = "config.ini";
iniParser.set("тест", "Моё значение");
Debug.Log(iniParser.get("тест"));
```
