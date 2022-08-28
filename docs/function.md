# Functions List
## BINPython info
`binpythoninfo.ver()` print Python and BINPython version   
`binpythoninfo.buildversion()` print buildversion   
`binpythoninfo.libs_warning()` Check if function warnings are enabled  
`binpythoninfo.releases_ver()` print releases version  
`binpythoninfo.build_importlibs()` Output custom built libraries (output import_libs)  
## Windows-only
`binpythonwin.setwindowtitle(<titlename>)` Set the window title, `<titlename>` is the window name, only a string  
## BINPython function
`binpython_welcome_text()` print welcome text  
`binpython_shell()` goto BINPython Shell
## BINPython Plugin
These functions are designed for BINPython Plugin, these codes should be written in your Plugin instead of using directly  
`binpythonplugin.name(<plugin_name>)` set plugin name, `<plugin_name>` is the plugin name, only a string  
`binpythonplugin.anthor(<anthor_name>)` set plugin anthor name, `<anthor_name>` is the plugin anthor name, only a string  
`binpythonplugin.description(<description>)` set plugin description, `<description>` is the plugin description, only a string  
`binpythonplugin.showinfo()` print plugin info(must be set (name, author, description))  