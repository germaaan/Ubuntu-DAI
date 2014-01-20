# Ubuntu-DAI 1.0

FROM    ubuntu
MAINTAINER German Martinez <germaaan@gmail.com> Version: 1.0

# Instalar todos los paquetes necesarios para poder realizar las prácticas de DAI
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv 7F0CEB10
RUN echo "deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen" | tee -a /etc/apt/sources.list.d/10gen.list
RUN apt-get update
RUN apt-get -y install apt-utils
RUN apt-get -y install python python-setuptools mongodb-10gen python-django
RUN sudo easy_install web.py
RUN sudo easy_install mako
RUN sudo easy_install pymongo
RUN sudo easy_install feedparser
RUN sudo easy_install tweepy 

# Configurar MongoDB
CMD ["/usr/bin/mongod", "--config", "/etc/mongodb.conf"] 
