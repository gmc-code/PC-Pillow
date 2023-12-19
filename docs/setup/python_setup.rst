==============================
Python Setup
==============================

Install Python
------------------------------

* Check the version of python installed from the command line.

.. code-block::

    python --version

* Download and install Python from https://www.python.org/downloads/.

----

Create a python Virtual environment
---------------------------------------

| See: https://www.youtube.com/watch?v=APOPm01BVrk
| Rather than installing the python packages in the system wide installation of python, a virtual environment can be created that only has the modules needed for your project.
| Virtual environments allow easy maintenance of the libraries needed for the project and avoid issues that can happen when multiple dependencies conflict across multiple projects.

| Create a virtual environment for the packages needed.
| By default, these will be created in the users directory: ``C:\Users\username\``.
| In examples below, the virtual environment folder will be called: ``rtd_venv``, but any suitable name can be used.

| Create a virtual environment, called **rtd_venv**, with the default system python:

.. code-block::

    python -m venv rtd_venv
    
| If there are different versions of python installed, use the full path to the version required to create the virtual environment.
| <username> used in the paths below will be different for each user.
| e.g. ``C:\Users\username\AppData\Local\Programs\Python\Python312\python.exe``
| Create a virtual environment using a specific installed version of python:

.. code-block::

    "C:\Users\username\AppData\Local\Programs\Python\Python312\python.exe" -m venv rtd_venv

Activate a python Virtual environment
---------------------------------------

| Before you can start installing or using packages in your virtual environment you'll need to activate it.
| Activating a virtual environment will put the virtual environment-specific python and pip executables into your shell's PATH.
| Opening a terminal inside Visual Studio Code will automatically activate the selected virtual environment.

| Activate the virtual environment:

.. code-block::
    
    "C:\Users\username\rtd_venv\Scripts\activate.bat"

----

Using the python Virtual environment in VSCode
---------------------------------------------

| VSCode allows the use of different python environments.
| To use the python python Virtual environment in VSCode:

    #. Choose **View: Command Palette**. 
    #. Into the drop down search field, type: **Python : Select Interpreter**
    #. Choose the one listed that refers to the newly created **rtd_venv**.

----

Updating pip
---------------------------------

| After setting up a project, there may be a need to update the pip.

.. code-block::

    python.exe -m pip install --upgrade pip

----

Installing packages
---------------------------------

* To install a package such as pillow, check the output from typing in the VSCode terminal:

.. code-block::

    pip install pillow


* To check the installed version numbers and other info about a package, such as pillow, check the output from typing in the VSCode terminal:

.. code-block::

    pip show pillow

----

Updating packages
---------------------------------

* To update installed packages, such as pillow, to the latest version, run pip install with the --upgrade or -U option.

.. code-block::

    pip install --upgrade pillow

----

List installed packages
------------------------------

* To get all the installed version numbers, check the output from typing in the VSCode terminal:

.. code-block::

    pip list

* To see if there are updates available, check the output from typing in the VSCode terminal:

.. code-block::

    pip list -o

* To list updates and those packages that don't need updates, check the output from typing in the VSCode terminal:

.. code-block::

    pip list --outdated



