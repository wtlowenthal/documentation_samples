# Poetry Package Manager Overview and Installation Guide
## Overview

The Poetry Package Manager for Python allows the user to declare all libraries used in the Python project. Poetry will manage each package by installing and updating it automatically.

Many users, experienced and new alike, find managing packages and dependencies cumbersome at best and aggravating at worst. Manually installing, updating, and maintaining them can lead to a myriad of problems, including conflicts, version changes, and formatting difficulties. 

Poetry allows the user to manage dependencies from a single file, *pyproject.toml*. This file replaces the standard Python files *setup.py*, *requirements.txt*, *setup.cfg*, *MANIFEST.in*, and Pipfile. This greatly simplifies the processes of dependency management, packaging, and publishing.

The package manager helps the user structure and manage their Python projects and allows easy configuration using the command-line interface and a single configuration file. In addition to handling dependency management, creating a new Python project using Poetry automatically creates the project's directory structure.

## Installation
Poetry requires Python 2.7 or 3.5+. Note that after Poetry version 1.2, Poetry will **not** support Python 2.7 and Python 3.5.

Poetry uses a custom installer instead of *pip*. Using *pip* to install Poetry may cause conflicts with other system files. Instead, follow one of the procedures described below.

### Installing to Linux/OSX
To install Poetry to a Linux or OSX environment, use the installer at the command line. The installer will install Poetry to the *bin* directory in the *.poetry* directory (*$HOME/.poetry/bin*). Enter the command:
>curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -

The installer will also add the directory to the **$PATH** environmental variable.

After installing, test the installation and environment by entering the command:
>poetry --version

### Installing to Windows Powershell
To install Poetry to a Windows Powershell environment, use the installer at the command line. The installer will install Poetry to the *bin* directory in the *.poetry* directory (*%USERPROFILE%/.poetry/bin*). Enter the command:
>(Invoke-WebRequest -Uri https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py -UseBasicParsing).Content | python -

After installing, test the installation and environment by entering the command:
>poetry --version

## Creating a New Project
### Create the New Project Directory ###
To create a new Python project using Poetry, first create a new directory using the command:
> poetry new projectname

Where *projectname* is the name of the project and directory. This command also populates the new directory with the required Python files and subdirectories.

### Specify Dependencies ###
To add dependencies to the project, edit the file *pyproject.toml* in the newly created directory. Add a separate line for each dependency under the section **[tool.poetry.dependencies]**, then enter the package name and version, separated by an equal sign (=) with the version number in quotations. To indicate the minimum version, enter a carrot (^) prior to the version number.
>[tool.poetry.dependencies]
>example_dependency = "^1.2"

Alternatively, instead of manually editing the *pyproject.toml* file, the user can add new dependencies using the command line:
> poetry add example_dependency

### Install Dependencies ###
To install the dependencies defined in the *pyporoject.toml* file, run the command:
>poetry install

If the project does not have an existing *poetry.lock* file, Poetry will resolve and install all dependencies listed in the file and download their latest versions. If Poetry already has an existing *poetry.lock* file, it will install the exact version listed in the file to make sure that package versions remain the same across all instances and users of the project.

### Commit the Project ###
Commit the project, including the *poetry.lock* file to the project repository.

## Additional Resources

### Uninstalling Poetry ###
To uninstall Poetry, use the command
>python get-poetry.py --uninstall

### External Resources ###
* https://python-poetry.org/docs/
* https://hackersandslackers.com/python-poetry-package-manager/
* https://blog.networktocode.com/post/upgrade-your-python-project-with-poetry/
