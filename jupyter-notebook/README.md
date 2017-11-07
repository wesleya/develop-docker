## Installation

1. copy docker-compose.yml into the directory containing your jupyter notebooks

2. run the docker container
```
$ docker-compose up
```
3. optional if you want to get a bash in the docker container
```
# find the name of the container
$ docker-compose ps

# get bash shell. jupyter notebooks are mapped to /opt/notebooks in the container
$ docker exec -it <name-of-container> bash
```

4. bring the container down when you're done with hugo
```
$ docker-compose down
```

