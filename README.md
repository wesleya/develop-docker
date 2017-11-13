Each directory in this repo contains my setup for starting a new project type. For example hugo directory is for starting a new hugo site.

## To Do

* figure out why we need the bind=0.0.0.0
* add instructions for just using a single command vs using the docker-compose.yml
* add instructions for manual build vs using the docker hub version
* add a setup for laravel projects
* add a setup for vanilla php projects

## Updating Images

```
# build latest image. tag it as new update (1.0) and tag it as latest. run this from directory with the Dockerfile
$ docker build -t wagena/develop-hugo:1.0 -t wagena/develop-hugo:latest .

# Log into Docker Hub from our CLI client
$ docker login

# Push up each tagged image
$ docker push wagena/develop-hugo:1.0
$ docker push wagena/develop-hugo:latest
```

## Viewing Containers

```
# list local images
docker images

# list running containers
docker ps
```

## Cleaning Up

If you're like me and make tons of mistakes and don't want the record of all your broken images and containers lying around, you can clean them them:

```
# remove a container: 
$ docker rm <Container ID>

# remove all containers: 
$ docker rm $(docker ps -a -q)

# remove images: 
$ docker rmi <Image ID>

# remove all images: 
$ docker rmi $(docker images -a -q) -f
```

Note: You must remove all containers using an image before deleting the image
