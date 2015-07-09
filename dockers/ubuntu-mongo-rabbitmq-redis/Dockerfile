
# This docker file packages a bunch of useful system services
# to make local testing and developing more seamless.

FROM ubuntu:15.04

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10

RUN echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | tee /etc/apt/sources.list.d/mongodb.list

RUN apt-get update -qy

RUN apt-get install mongodb-10gen=2.4.14 -qy

RUN apt-get install redis-server -qy

RUN apt-get install rabbitmq-server -qy

RUN mkdir /data && mkdir /data/db

RUN echo "[{rabbit, [{loopback_users, []}]}]." > /etc/rabbitmq/rabbitmq.config

CMD redis-server & mongod & rabbitmq-server
