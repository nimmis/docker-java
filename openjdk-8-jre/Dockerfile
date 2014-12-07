FROM ubuntu:14.04

MAINTAINER nimmis <kjell.havneskold@gmail.com>

# disable interactive functions
ENV DEBIAN_FRONTEND noninteractive

# set default java environment variable
ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64

RUN apt-get update 
RUN apt-get install -y openjdk-8-jre-headless
RUN rm -rf /var/lib/apt/lists/*

#set default command
CMD ["bash"]

