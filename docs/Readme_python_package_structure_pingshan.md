# Python packaging authority
https://packaging.python.org/en/latest/tutorials/packaging-projects/

## src: 
all project code should be in src directory, and sorted in various sub_directories.
## pyproject.toml: 
all modern python projects should have pyproject.toml file. To store python specific meta data. This is especially immportant if the package is meant to be distributed and used by other people.
## \_\_init\_\_.py
inside a folder: this file makes a folder into a "package" so that one can import the name of the directory as a package directly. The body of the file includes what is availabe to users when the package is imported. In addition, any code in the __init__.py file will be run exactly one time when the package is imported. This allows the initialization of a package, for example importing other dependent packages without users handling or even knowing them.
## LICENSE, README.md, .gitignore: 
duh
## setup.py: 
the file contains the instructions for how the package is bundled and published. This script is run when the package is installed with pip or other commends such as. 
```bash
    $ python setup.py sdist bdist_wheel
```
Running this command would result in 2 folders:
1. build folder: 
2. dist folder: .whl and .tar.gz files can be distributed to other users. 
3. dist file installation:
```bash
    $ pip install dist/package_name_version.whl
```
## __main__.py 
run as '__main__' when you run a package as the main program.
## Tests: 
having a __main__.py module would make things a lot easier. A test can be run simply by executing 
```bash
    $ py -m tests
```


# dunder functions:
__init__.py is run when you import a package into a running python program. For instance, import idlelib within a program, runs idlelib/__init__.py, which does not do anything as its only purpose is to mark the idlelib directory as a package. On the otherhand, tkinter/__init__.py contains most of the tkinter code and defines all the widget classes.

For instance, python -m idlelib at a command line runs idlelib/



