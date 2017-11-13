FROM ubuntu:17.10 

LABEL maintainer="Wesley Agena"

# Create working directory
RUN mkdir /root/site
WORKDIR /root/site

RUN apt-get update
RUN apt-get -y install vim
RUN apt-get -y install nodejs npm
RUN npm install --global gulp-cli
RUN npm install --global gulp
RUN npm install --global node-sass
RUN npm install --global gulp-sass
RUN npm rebuild node-sass

# By default, run gulp watch
CMD ["gulp", "watch"]
