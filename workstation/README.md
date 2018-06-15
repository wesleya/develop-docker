docker build -t wagena/workstation:1.0 -t wagena/workstation:latest .

docker run --rm -it wagena/workstation bash
docker run --rm -it wagena/workstation zsh
docker run --rm -it wagena/workstation 


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
