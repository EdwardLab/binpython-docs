# Write your plugin
BINPython supports plugins. You can write your own functions and classes to load into the plugin  
# Create your plugin
Create a `binpython_plugin` folder in your BINPython run directory   
This folder should contain two files:`pluginconfig.binpython` and `function.py`  
After creating the file, by any method, such as IDE or file editor, enter the following content in the specified file below:  
pluginconfig.binpython：  
```
binpythonplugin.loadmain("function.py")
```

function.py:
```
binpythonplugin.name("Your Plugin name")
binpythonplugin.anthor("Plugin Anthor")
binpythonplugin.description("Plugin description")
```
In the pluginconfig.binpython file, the code: binpython_plugin_loadmain("function.py") means to load the plugin function from function.py, function.py can be any file

function.py must contain binpythonplugin.name, binpythonplugin.anthor, binpythonplugin.description These functions describe the basic information of this plugin, you can directly change the above template information, the content must be a string   
For functions for plugin information, see the "BINPython function" chapter

Then write your function code in function.py, for example, here is a simple example:
```
binpythonplugin.name("BINPython demo plugin")
binpythonplugin.anthor("Edward")
binpythonplugin.description("Simple BINPython example")

import os
class binpython_demo():
    def hello():
        print("hello BINPython")
    def linuxuname():
        os.system("uname -a")
    def winver():
        os.system("winver")
```
You can view plugin info anywhere with `binpythonplugin.showinfo()`