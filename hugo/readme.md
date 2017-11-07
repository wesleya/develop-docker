## Installation

1. copy docker-compose.yml into the root directory of your hugo project

2. run the docker container
```
$ docker-compose up
```
3. optional if you want to get a bash in the docker container
```
# find the name of the container
$ docker-compose ps

# you'll land in the ~/site which is mapped to your hugo site root directory on your host machine
$ docker exec -it <name-of-container> bash
```

4. bring the container down when you're done with hugo
```
$ docker-compose down
```

## Notes

* The docker container does not pick up changes made on the host machine. 
* It does pick up changes made on the guest machine through the bash command
