
```
# build the docker image
$ docker build -it hugo-server .

# copy the example docker-compose.yml file into the root directory of the hugo project as docker-compose.yml

# run bring up the docker container
$ docker-compose up

# find the name of the container
$ docker-compose ps

# get a bash shell to make changes
$ docker exec -it bookbreakdowns_develop_1 bash
```

## Notes

* The docker container does not pick up changes made on the host machine
* It does pick up changes made on the guest machine through the bash command

## To Do

* commit the image and push it up to docker repository
* when you do this change the Dockerfile and docker-compose.yml to use the new image name
* figure out how to use zsh instead of bash