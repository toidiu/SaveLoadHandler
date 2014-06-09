SaveLoadHandler
===============

Android GSON based save/load handler. Type is declared when creating a new instance so each handler is independent and of others.

##Usage
1 Create an instance of the SaveLoadHandler:
```
  Type type = new TypeToken<ArrayList<CLASS>>(){}.getType();
  SaveLoadHandler<ArrayList<CLASS>> = new SaveLoadHandler(type, SAVE_FILE);
```
  replace the 'CLASS' with your custom class. Gson will take care of converting the data type into JSON.

2 Thats it! Now save and load some data. There are currently no checks if the file is empty and a load data is attempted.
```
slh.saveData(this, list);
list = this.slh.loadData(this);
```


--Created by Apoorv Kothari--
