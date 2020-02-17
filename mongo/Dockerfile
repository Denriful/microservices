FROM ubuntu:16.04

#RUN apt-get update
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv D68FA50FEA312927
RUN bash -c 'echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" > /etc/apt/sources.list.d/mongodb-org-3.2.list'
RUN apt-get update
RUN apt-get install -y mongodb git

COPY mongodb.conf /etc/mongodb.conf
COPY db_config /reddit/db_config
COPY start.sh /start.sh


RUN chmod 0777 /start.sh

CMD ["/start.sh"]