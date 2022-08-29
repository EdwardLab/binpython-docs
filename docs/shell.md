# BINPython Shell
BINPython has a built-in shell emulation interpreter, which can parse Python statements like the following:
```
BINPython x.xx-build-full-officalplus-building (Python Version:x.xx.x)By:XINGYUJIE https://github.com/xingyujie/binpython[Running on OSNAME]
Type "about", "help", "copyright", "credits" or "license" for more information.
>>>
```
You can enter the Python statement you want to execute after `>>>`, and it will be executed after pressing Enter, yes, this is the same as the Python standard interpreter   
However, the only difference from the standard Python interpreter is that it does not support multi-line statements like these:
```
for i in range(10):
...
while True:
...
```
Because the interactive mode of the BINPython simulation actually uses the script mode to run, the interactive mode is not supported. However, you can run through IDEPlus, BINPython IDLE, or run the script file directly, we cannot guarantee that this problem will be fixed