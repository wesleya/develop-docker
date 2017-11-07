these are docker files I use for developing my side projects

## To Do

* figure out why we need the bind=0.0.0.0
* add instructions for just using a single command vs using the docker-compose.yml
* add instructions for manual build vs using the docker hub version

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

## Cleaning Up

If you're like me and make tons of mistakes and don't want the record of all your broken images and containers lying around, you can clean them them:

```
# remove a container: 
$ docker rm <Container ID>

# remove all containers: 
$ docker rm $(docker ps -a -q)

# remove images: 
$ docker rmi <Container ID>

# remove all images: 
$ docker rmi $(docker ps -a -q)
```

Note: You must remove all containers using an image before deleting the image
