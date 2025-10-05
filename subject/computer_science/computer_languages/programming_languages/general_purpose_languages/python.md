--- 
title: Python
tags: ["programming language", "scripting language", "python"]
---

## Download & Install

### Install in Linux

1. APT Package Manager
   1. `sudo apt update`: General command to always run, updates your packages list
   2. `sudo apt install python3`: Install Python 3 (if not already installed or to ensure latest version from repositories)
   3. `sudo apt install python-is-python3`: [Optional] Even after above python3 installation, by default the python command won't initiate the python instance, the python-is-python3 package is specifically designed for Debian-based Linux distributions like Ubuntu. It creates a symbolic link that points the python command to the default python3 interpreter, allowing users to execute Python 3 scripts using the python command instead of python3. In Past python was associated with python 2 has been stopped from further development and maintenance.

## How to

### Create Virtual Environment

#### In Linux 

- `python -m venv .venv`: to create a virtual environment named .venv in a particular directory.
- But With just python installed using `sudo apt install python3`, the virtual environment might not get created because of ensurepip unavailability. Hence first run `sudo apt install python3-venv`
- 