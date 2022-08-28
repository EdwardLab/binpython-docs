# How to configure startup files
BINPython supports configuring default startup files. When the `startupfile.conf` file is created, BINPython will read the file name in `startupfile.conf` and run it. You just need to create `startupfile.conf` and fill in the startup file name or absolute path. The next time you start BINPython it will automatically read the filename in startupfile.conf and run this script   

Simply put, you just need to create a `startupfile.conf` file and fill in the startup script file name in `startupfile.conf`

For example, if I want to start `hi.py` when I open BINPython, I just need to create `startupfile.conf` and fill in `hi.py` into `startupfile.conf`. The next time BINPython is opened, `hi.py` will be run first.