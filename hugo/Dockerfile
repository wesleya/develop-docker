FROM ubuntu:17.10

LABEL maintainer="Wesley Agena"

RUN apt-get update
RUN apt-get -y install hugo
RUN apt-get -y install vim
RUN apt-get -y install git
RUN apt-get -y install nodejs npm
RUN apt-get -y install wget
RUN sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

EXPOSE 1313

# Create working directory
RUN mkdir /usr/share/site
WORKDIR /usr/share/site

# By default, serve site
ENV HUGO_BASE_URL http://localhost:1313
CMD hugo server -b ${HUGO_BASE_URL} --bind=0.0.0.0

# docker build --no-cache -t hugo-server .