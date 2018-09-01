## To Do

* add better notes on how this should work
* add a config file for choosing a different zsh theme (one that includes full path)
* figure out how to install my vim settings
* get laravel working

```
// build any updates
$ docker build -t wagena/workstation:1.0 -t wagena/workstation:latest .

// push after build
$ docker push wagena/laravel:1.0 
$ docker push wagena/laravel:latest

docker run --rm -it wagena/workstation bash
docker run --rm -it wagena/workstation zsh
docker run --rm -it wagena/workstation 
```

## Docker Compose

# check what containers are up
docker-compose ps

# run zsh (or any other command from workstation service)
docker-compose up -d 
docker-compose exec workstation zsh

# start up a new 
docker-compose run workstation

# remove services
docker-compose down

## Remove/Stop Containers/Images

```
# List all containers (only IDs)
$ docker ps -aq

#Stop all running containers
$ docker stop $(docker ps -aq)

# Remove all containers
$ docker rm $(docker ps -aq)

# Remove all images
$ docker rmi $(docker images -q)
```
