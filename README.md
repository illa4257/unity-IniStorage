# IniStorage for Unity - Working with ini files in Unity!

* Code can be changed! :)

* Tested on Unity:
  - 2021.2.7f1

In Unity forum: [**https://forum.unity.com/threads/read-write-ini-file.857215/**](https://forum.unity.com/threads/read-write-ini-file.857215/)

---

### How to put?

Move the [**script**](https://github.com/illa4257/iniStorageForUnity/releases) to the project.

### Example:
Code:
```c#
var ini = new IniStorage(Application.dataPath + "/config.ini");

if(!ini.Contains("Test"))
    ini.Set("Test", "Test string")
        .ClearComments()
        .AddComment("Test comment")
        .AddComment("Test comment 2");

if (!ini.Contains("Test2"))
    ini.Set("Test2", "Test string");

if (!ini.Contains("Test3"))
    ini.Set("Test3", "Test string");

if (!ini.Contains("Test4"))
    ini.Set("Test4", "Test string")
        .AddComment("Test comment");

if (!ini.Contains("Test5"))
    ini.Set("Test5", "Test string");

if (!ini.Contains("TestGroup", "Test"))
    ini.Set("TestGroup", "Test", 5.545434f)
        .ClearComments()
        .AddComment("Test group pair comment");

if (!ini.Contains("TestGroup", "Test2"))
    ini.Set("TestGroup", "Test2", "Test value");

ini.GetGroup("TestGroup")
    .ClearComments()
    .AddComment("Test group comment!");

if (!ini.Contains("TestGroup", "Test3"))
    ini.Set("TestGroup", "Test3", "Test value 2");

if (!ini.ContainsEndComment("End comment"))
    ini.ClearEndComments()
        .AddEndComment("End comment")
        .AddEndComment("End comment 2");

ini.Save();

Debug.Log(ini.GetStringOrDefault("Test", "None"));
Debug.Log(ini.GetFloat("TestGroup", "Test"));
Debug.Log(ini.GetFloatOrDefault("TestGroup", "Test2", 0f));
```

config.ini:
```ini
#Test comment
#Test comment 2
Test=Test string
Test2=Test string
Test3=Test string
Test4=Test string
Test5=Test string

#Test group comment!
[TestGroup]

#Test group pair comment
Test=5,545434
Test2=Test value
Test3=Test value 2

#End comment
#End comment 2
```

Logs:
```
Test string
5.545434
0
```