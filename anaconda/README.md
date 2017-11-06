# build the docker image
$ docker build -it anaconda .

# copy the example docker-compose.yml file into the root directory of the hugo project as docker-compose.yml

# run bring up the docker container
$ docker-compose up

# find the name of the container
$ docker-compose ps

# get a bash shell to make changes
$ docker exec -it introductiontodatascienceinpython_develop_1 bash
