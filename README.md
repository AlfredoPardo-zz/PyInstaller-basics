# PyInstaller-basics
Making a Single Executable File with PyInstaller

## Introduction

* Taking the output files of my [Cython Basics PoC](https://github.com/AlfredoPardo/cython-basics), I wanted to make a single executable from them and this could not be easier.
* PyInstaller reads a Python script, discovers every other module and library the script depends on, collects copies of those files including the Python interpreter and puts them in a single file.
* There is no need to have Python installed to run the output file.

### Steps to reproduce it

##### 1. Using the already created Virtual Environment, install the PyInstaller package
```bash
$ pip install pyinstaller
```

##### 2. Running the command with the --onefile option will create a *dist* folder and within it the new binary executable to distribute (along with the *build* folder and the *.spec* file at the same level)
```bash
$ pyinstaller --onefile run_modules.py
```

##### 3. It can be run as a standard linux executable
```bash
$ ./dist/run_modules
```

#### Additional Notes

+ I left the files as they finished on my folders for this PoC, except for the *env* directory used for the Virtual Environment.