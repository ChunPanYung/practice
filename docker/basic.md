### Basic Commands

`$ docker pull IMAGES`: Pull images from docker hub website
<<<<<<< HEAD
`$ docker run IMAGES`: Running a single image as container

`$ docker images`: List all images

`$ docker ps`: List all current running containers
`$ docker ps --all`: List all containers, whether it's running or not


### Technical Terms
* Images: actual packages, artifact
* Containers: actually start the application
=======
`$ docker rmi IMAGES_ID`: Remove docker image according to its ID
`$ docker images`: List all images
&nbsp;
`$ docker ps`: List all current running containers
`$ docker ps --all`: List all containers, whether it's running or not
&nbsp;
`$ docker [start|stop] IMAGES_ID`: Running a single image as container
`$ docker container rm CONTAINER_ID`: Remove container by its ID
&nbsp;
`$ docker logs CONTAINER_ID`: view logs of container
`$ docker exec --interacitve --tty CONTAINER_ID /bin/TERMINAL`: Run commands within container in interactive terminal mode.
&nbsp;
`$ docker network ls`: list of network that can be used by docker container
`$ docker network create NETWORK`: create a new network named NETWORK
&nbsp;
`$ docker build --tag my-app:1.0 /DIRECTORY`: build a docker images from directory, not file

##### Command:`$docker run`

`$ docker run IMAGES`: Running a single image as container
`$ docker run IMAGES:VERSION`: Pull images and starts container by image version
`$ docker run --detach IMAGES`: Running  a container in detached mode
`$ docker run --publish HOST_PORT:CONTAINER_PORT IMAGES`: Bind the host port to container port
`$ docker run --name NEW-NAME IMAGE_ID`: create a new container named NEW-NAME

### Docker-Compose

`$ docker-compose --file FILE.yaml up`: Execute docker command written in yaml and start up all containers in detached mode

### Dockerfile

`FROM`: Image based on
`ENV`: Environmental variables
`RUN`: Execute Linux Command (insde the app container)
`COPY`: Copy from the host machine to guest image
`CMD`: entrypoint command, just one command and final command

* Whenever you change Dockerfile, you have to rebuild image

### Technical Terms

* Images: actual packages, artifact

* Containers: actually start the application

* port binded to container: Port 5000

* To communicate with containers:
  
  * create docker network
  * connect them using container name/ID (read docker image doc)
>>>>>>> docker
