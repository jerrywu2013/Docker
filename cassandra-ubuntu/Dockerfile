FROM docker.io/jerryspark/ubuntu
MAINTAINER Jerry Wu <rippleblue2002@gmail.com>

RUN add-apt-repository ppa:webupd8team/java \
    && apt-get update \
    && apt-get -y install oracle-java8-set-default 

RUN echo "deb http://www.apache.org/dist/cassandra/debian 22x main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list \
    && echo "deb-src http://www.apache.org/dist/cassandra/debian 22x main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list \
    && sudo apt-get update \
    && gpg --keyserver pgp.mit.edu --recv-keys 749D6EEC0353B12C \
    && gpg --export --armor 749D6EEC0353B12C | sudo apt-key add - \
    && gpg --keyserver pgp.mit.edu --recv-keys 2B5C1B00 \
    && gpg --export --armor 2B5C1B00 | sudo apt-key add - \
    && gpg --keyserver pgp.mit.edu --recv-keys 0353B12C \
    && gpg --export --armor 0353B12C | sudo apt-key add -\
    && sudo apt-get update

RUN apt-get -y install cassandra

EXPOSE 9042 7199 7000 7001 9160 9042
