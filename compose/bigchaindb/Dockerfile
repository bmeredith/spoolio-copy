FROM python:3.5

RUN apt-get update

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

RUN wget https://github.com/bigchaindb/bigchaindb/archive/refs/tags/v1.0.1.tar.gz
RUN mkdir bdb
RUN tar xvf v1.0.1.tar.gz -C bdb --strip-components 1

WORKDIR /usr/src/app/bdb

RUN python setup.py install
WORKDIR /usr/src/app
RUN rm -r bdb master
