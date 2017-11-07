these are docker files I use for developing my side projects

## To Do

* commit docker images to docker hub, then update docker-compose files to pull the hub version. (don't require manual build)
* figure out why we need the bind=0.0.0.0
* add instructions for just using a single command vs using the docker-compose.yml
* add instructions for manual build vs using the docker hub version

## Commit Updated Image

```
# build new image
$ docker build -t hugo-server .

# run new image
$ docker run -t -i hugo-server /bin/bash

# exit out of the bash you just started
$ exit

# get list of all containers that were run
$ docker ps -a

# commit the updated image
$ docker commit c94b90777a04 wagena/develop-hugo:0.1
$ docker commit c94b90777a04 wagena/develop-hugo:latest
```
