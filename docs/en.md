# English documentation

* Object iniStorage
  - iniStorage.path - path to ini file (If there is no file, then the script itself will create it when you call some function!), default path is dataPath/config.ini
  - [**iniStorage.set(string key, string value) : void**](#inistoragesetstring-key-string-value--void)
  - [**iniStorage.get(string key) : string**](#inistoragegetstring-key--string)

## iniStorage.set(string key, string value) : void

### Information

Sets the value for the key in the ini file

### Accepts parameters:

key - key name

value - key value

### He does not return anything

## iniStorage.get(string key) : string

### Information

Gets the key value from an ini file

### Accepts parameters:

key - key name

### Returns the ini file key value