# Custom configure and personalize your BINPython
BINPython has built-in personalization and customization functions, you can create `binpython_config` in the BINPython run directory to enable this function  

When you create the `binpython_config` folder, you will find that nothing changes, because you also need to create three configuration files, these three configuration files can contain one also can include all, they are:

 `help.txt` -- When you create `help.txt` in `binpython_config` folder and use `binpython -h (--help)`, BINPython will not load the default help information, you will see, it will output the content of help.txt file, which can help you Define help content for BINPython

 `version.py` -- This is a Python script file, when you run `binpython -v (--version)` when you create version.py under `binpython_config` folder, BINPython will not run the default version information, it will run `version.py`

 `welcome.py` -- This is also a Python script, but the difference is that when you open the BINPython Shell, it will not output the default BINPython information, like this:

 ```
 BINPython versioncode-build-full-officalplus-building (Python Version:x.xx)By:XINGYUJIE https://github.com/xingyujie/binpython[Running on OSNAME]
Type "about", "help", "copyright", "credits" or "license" for more information.
```

When the existence of `welcome.py` is recognized, the default text information will be deleted when the BINPython Shell is opened. Like the above text, you can use print in welcome.py to output your favorite questions, add custom functions, etc.