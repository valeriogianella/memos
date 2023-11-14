# Docker set up and commands for django project
We suppose that a virtual enviroment for the django project has already been set up, and the packages have been registered in the requirements file.

Create a file **Dockerfile** specifying the base image <image> and <working_directory>
````
# Pull base image
FROM <image>

# Set environment variables
ENV PIP_DISABLE_PIP_VERSION_CHECK 1
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work direcotry
WORKDIR /<working_directory>

# Install dependencies
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# Copy project
COPY . .
````
Add an ignore file **.dockerignore**
````
.venv
.git
.gitignore
.vscode
````
### Build a docker image
````
docker build .
````
*The image is ready to be run as a container, add the docker-compose.yml and start the container*  
**docker-compose.yml**
````
version: "2"
services:
  ...

volumes:
  ...
````
### Start docker container, -d for detached mode
````
docker-compose up -d
````
### Stop the container
````
docker-compose down
````
### Run commands <command> in docker using the service <service> (specified in the **Dockerfile**)
````
docker-compose exec <service> python manage.py <command>
````
e.g.
````
docker-compose exec web python manage.py runserver
````
