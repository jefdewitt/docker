# Docker
This is a Docker testing ground for me to learn all about containers and all that jazzy nomenclature.

## Cheat Sheet

### List Docker CLI commands

	$ docker
    $ docker container --help

### Display Docker version and info

	$ docker --version
    $ docker version
    $ docker info

### Execute Docker image

	$ docker run hello-world

### List Docker images

	$ docker image ls

### List Docker containers (running, all, all in quiet mode)

	$ docker container ls
    $ docker container ls -all
    $ docker container ls -a -q
	
### Build an image

	// The -t is for making a human-readable name
	$ docker build -t <friendly-name> .
	
### Run a detached image in the background

	// The -d is the detached flag and can be removed to make process run in foreground
	// -p = publish
	$ docker run -d -p 4000:80 <friendly-name>
	
### Stop the process

	// Get the container ID from $ docker container ls or use the name you assigned it instead
	$ docker container stop 1fa4ab2cf395
	
### Remove <none> images 

	$ docker system prune
	
### Remove exited containers

	// ps = process status
    $ docker rm $(docker ps -a -f status=exited -q)

### Remove all existing containers

    docker ps -a | awk '{print $1}' | while read -r id ; do
        docker rm -f $id
    done
