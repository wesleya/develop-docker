FROM ubuntu:18.04

LABEL maintainer="Wesley Agena"

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update

# install any programs I use
RUN apt-get -y install vim curl zip unzip git wget tmux zsh

# this is so the php7 installs don't ask us for timezone input
RUN apt-get update \
    && apt-get install -y gnupg tzdata \
    && echo "UTC" > /etc/timezone \
    && dpkg-reconfigure -f noninteractive tzdata

# install php7
RUN apt-get -y install php7.2-fpm php7.2-cli \
       php7.2-pgsql php7.2-sqlite3 php7.2-gd \
       php7.2-curl php7.2-memcached \
       php7.2-imap php7.2-mysql php7.2-mbstring \
       php7.2-xml php7.2-zip php7.2-bcmath php7.2-soap \
       php7.2-intl php7.2-readline php7.2-xdebug \
       php-msgpack php-igbinary

# install composer
RUN php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer

# cleanup
Run apt-get -y autoremove \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# create my user and set my working directory
 RUN useradd -ms /bin/bash wagena
USER wagena
WORKDIR /home/wagena

RUN git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh \
	&& cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

# run this command by default
CMD ["zsh"]
