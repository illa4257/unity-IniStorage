# Документация на русском

* Объект iniStorage
  - iniStorage.path - путь к ini-файлу(Если файла нет, сам скрипт создаст его при вызове какой-либо функции!), изначальный путь dataPath/config.ini
  - [**iniStorage.set(string key, string value) : void**](#iniStorage-setstring-key-string-value--void)
  - [**iniStorage.get(string key) : string**](#iniStorage-getstring-key--string)

## iniStorage.set(string key, string value) : void

### Информация

Устанавливает значение для ключа в ini-файле

### Принимает параметры:

key - имя ключа

value - значение для ключа

### Он ничего не возвращает

## iniStorage.get(string key) : string

### Информация

Получает значение ключа из ini-файла

### Принимает параметры:

key - имя ключа

### Возвращает значение ключа ini-файла