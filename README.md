# Django Docker

This is template repository to build your ****django docker**** setup quickly and start working immediately.

## Features
- Local Docker Setup
- Docker Swarm Production Setup(Coming Soon)

### Steps

Use the template or download the repository
- Go to root/docker_files directory
- Update requirements.txt inside docker_files dir
- Create env docker image using command: *docker build -t my_django_env . -f DockerfileEnv*
- Go back to root directory
- run command *docker-compose -f docker_files/docker-compose-local.yaml run my_django_service django-admin.py startproject my_project*
    - This will create the default files and diretories for django project named **my_project**
- run command *docker-compose -f docker_files/docker-compose-local.yaml up*
    - This will up the services mentioned in docker compose local file
- wait for the services to come up
- got to localhost:8000 to check the default django page
- it's done    



### Conventions used this project
- Separate docker_files directory to keep all local and production docker setup and configuration files
- Separate files for local and production swarm setup
- Data directory to hold the mysql/mariadb persistent files to keep the state saved to disk
- *my_project* is the name of project here, change it accordingly