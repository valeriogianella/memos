# Create and set up virtual environment
### Create a virtual environment *venv* in the current folder
with python -m we run the following command as a command in python
```
python -m venv .venv
```
### Activate the venv
(from the folder where .venv is)
```
.venv\Scripts\activate
```
*All the following commands are meant to be executed in the activated virtual environment, they can be preceded by python -m*
### Install a package *<package>*, specify the version
````
python -m pip install <package>~=4.0.0
````
### Uninstall a package *<package>*
````
python -m pip uninstall [options] <package>
````
### Write or update the requirement file
````
python -m pip freeze > requirements.txt
````
### Install from requirements, update the packages
````
python -m pip install -r requirements.txt --upgrade
````
### Uninstall packages from the requirements
````
python -m pip uninstall -r requirements.txt
````
### List the installed packages
````
python -m pip list
````
