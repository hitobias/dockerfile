# This dockerfile uses the ubuntu image
# VERSION 1
# Author: hitobias
# Command format: Instruction [arguments / command] ..


FROM ubuntu:12.04
MAINTAINER hitobias hitobias@email.com

ENV CHURCHLIFE_DB churchlife
ENV APP_ROOT /var/www/www.chlife-stat.org

RUN apt-get update
#install apache2 & php5 & openssh-server
RUN apt-get -y install apache2 php5 php5-mysql php5-gd openssh-server vim
RUN a2enmod ssl rewrite


#install mariadb-server 10
RUN apt-get -y install python-software-properties
RUN apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xcbcb082a1bb943db
RUN add-apt-repository 'deb http://ftp.yz.yamagata-u.ac.jp/pub/dbms/mariadb/repo/10.0/ubuntu precise main'

RUN apt-get update
RUN apt-get install mariadb-server

#ADD start.sh start.sh
#CMD ["/start.sh"]

EXPOSE 80