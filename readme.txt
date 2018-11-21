PyCharm develop Pipenv projects

Pipenv:
The officially recommended Python packaging tool from Python.org

structures:
Pipfile      - specify which library to use
Pipfile.lock - specify libraries' version

Create projects

1/ "New Projects" set "Project Interpreter"'s
OR
2/ inside project set "PyCharm" -> "Preferences" -> "Project Interpreter"


3/ click "gear" -> "add" -> "Pipenv" -> "Install packages from Pipenv"

------------------------------------------------------------------------------------------------

Package management

1/ from terminal (iterm2 OR terminal) perform libraries management

2/ from PyCharms' terminal perform libraries management

Basic features of Pipenv

Enables truly deterministic builds, while easily specifying only what you want.
Generates and checks file hashes for locked dependencies.

Automatically install required Pythons, if pyenv is available.
(brew install pyenv)

Automatically finds your project home, recursively, by looking for a Pipfile.
(Pipfile is for like a list of requirement to be installed)

Automatically generates a Pipfile, if one doesn’t exist.

Automatically creates a virtualenv in a standard location.

Automatically adds/removes packages to a Pipfile when they are un/installed.

Automatically loads .env files, if they exist.

------------------------------------------------------------------------------------------------

To initialize a Python 3 virtual environment, run $ pipenv --three.
To initialize a Python 2 virtual environment, run $ pipenv --two.

------------------------------------------------------------------------------------------------


The main commands are install, uninstall, and lock, which generates a Pipfile.lock.
These are intended to replace $ pip install usage, as well as manual virtualenv management
(to activate a virtualenv, run $ pipenv shell).

0/ browse into the project location
in iterm2 -

1/ start by
$ pipenv install
creates Pipfile, Pipfile.lock (freeze package name, version, dependency)

2/ install new packages in the virtual environment
$ pipenv install python
$ pipenv install matplotlib
$ pipenv install numpy
$ pipenv install pytest

3/ uninstall packages
$ pipenv uninstall numpy

4/ show dependency tree
$ pipenv graph

5/ install packages for development environment
pipenv install --dev nose2

6/ install all packages specified in Pipfile.lock.
$ pipenv sync

7/ declares all dependencies
$ pipenv lock

8/ check against python style guide
$ pipenv check

9/ run python project
a - in PyCharm - set Interpreter
b - in shell
$ echo "backend: TkAgg" >> ~/.matplotlib/matplotlibrc
$ pipenv shell

10/ exit shell
$ exit

11/ to use the same libraries again
browse into the project location
open in PyCharm

------------------------------------------------------------------------------------------------


where are libries of Pipenv installed

~/.local/share/virtualenvs/pipenv_demo-FBS_I2wS/