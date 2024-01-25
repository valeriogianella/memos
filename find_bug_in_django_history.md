### Clone a repository <git-url>
```
git clone <git-url>
```
### Checkout a branch
Reset possible changes on the current branch
```
git restore .
```
SHA is the key of the commit
```
git checkout SHA
```
### Restore the files from the requirements.txt
````
python -m pip install -r requirements.txt --upgrade
````
### Run the commands to set up the environment
````
python manage.py makemigrations
python manage.py migrate
python manage.py collectstatic --noinput
python manage.py runserver
````
all the commands can be executed consecutively chaining them with &
