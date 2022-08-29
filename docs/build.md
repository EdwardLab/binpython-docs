# You can build BINPython yourself or use our Releases, this article will guide you to build BINPython yourself
1. Install the Python environment and Pypi, see https://python.org for details
2. Pull the repository through git
`git clone https://github.com/xingyujie/binpython.git`
3. Install the Python dependency library with the following command:  

`cd binpython`   

`pip install -r requirements.txt`

* notice: In Linux or multiple Python environments, pip may be pip3, see the system environment variables for details

4. If your system is Linux, use `bash buildlinux.sh`, if your system is Windows, double-click `buildwin.bat`  

(If you want to build tkinter in Linux, please install the `python3-tk` package (different Linux versions have different installation methods)
# Advanced
## build custom library
BINPython allows custom Python libraries to be built into BINPython for portable/integrated products

First we need to open BINPython's main file `binpythonfull.py` via any IDE or text editor

When opened, it should look like this:
```
"""
 @header binpython.py
 @author xingyujie https://github.com/xingyujie
 @abstract BINPython main file
"""

#BINPython By:XINGYUJIE AGPL-V3.0 LICENSE Release
#Please follow the LICENSE AGPL-V3
#full version
####################################
#build configure

ver="0.32-build-full"

libs_warning="1"
#1 is ture 0 is false.
#Changing the value to 0 will close the prompt that the library does not exist

buildversion = "plus" #plus version and standard version

releases_ver="offical" + buildversion + "-building"

importlibs="os" #Don't use "import xxx" 
#Imported library name, please use "importlibs="<library name>" instead of "import <library name>"
#Please note: The "importlibs" function does not support loading functions (such as from xxxx import xxxx, if necessary, please write it in the following location. However, please note that this operation may have the risk of error reporting, please report issues or solve it yourself
#xxxxxxxxxxxxxx

#from xxxx import xxxx
#xxxxxxxxxxxxxx
####################################
.......
```

We just need to change the code of #######...########...  

This code includes version information for the build as well as various configurations   

You can import the library you need by `importlibs="<library name>"`, or use `import <library name>` anywhere in the code

## The size is too large after packing BINPython?

pyinstaller may package some redundant libraries, which makes the packaged BINPython take up a lot of disk space. At this time, we need to use `pipenv` to create a virtual clean pip environment and install only the libraries needed by BINPython, so that the packaged BINPython will not be installed. Redundant libraries are included in BINPython, and there is no need to delete redundant libraries from the computer.

### install pipenv
Just `pip install pipenv`
how to use? See: https://pipenv.pypa.io/en/latest/

## Configure BINPython packaging information
BINPython uses the PyInstaller spec, you can find the `binpythonfull.spec` file in the BINPython source directory, which is the packaged spec configuration file of BINPython, which can configure the packaged icon and various options

See: https://pyinstaller.org/en/stable/spec-files.html
## Use another packaging tool?
Of course it can. It's just that we haven't tried it. BINPython uses the PyInstaller packaging tool by default. You can try other packaging tools, and if you find anything new, please submit a pull request or open an issue to us!