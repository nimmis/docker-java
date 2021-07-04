FROM nimmis/ubuntu:20.04

MAINTAINER nimmis <kjell.havneskold@gmail.com>

# disable interactive functions
ENV DEBIAN_FRONTEND noninteractive

# set default java environment variable
ENV JAVA_VERSION_MAJOR=11 \
    JAVA_TYPE="" \
    JAVA_OPT=openj9 \
    JAVA_HOME=/usr/lib/jvm/default-jvm \
    PATH=${PATH}:/usr/lib/jvm/default-jvm/bin/

RUN add-apt-repository ppa:openjdk-r/ppa -y && \

    # update data from repositories
    apt-get update && \

    # upgrade OS
    apt-get -y dist-upgrade && \

    # Make info file about this build
    printf "Build of nimmis/java:openjdk-$JAVA_VERSION_MAJOR-$JAVA_OPT$JAVA_TYPE, date: %s\n"  `date -u +"%Y-%m-%dT%H:%M:%SZ"` > /etc/BUILDS/java && \

    # get name of dist
    export CNAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2) && \

    # req. packages
    apt-get install -y wget apt-transport-https gnupg && \

    # get pgp key

    wget https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public && \
    gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --import public && \
    gpg --no-default-keyring --keyring ./adoptopenjdk-keyring.gpg --export --output adoptopenjdk-archive-keyring.gpg && \
    rm public adoptopenjdk-keyring.gpg && \
    mv adoptopenjdk-archive-keyring.gpg /usr/share/keyrings && \

    # Configure AdoptOpenJDK's apt repository
    echo "deb [signed-by=/usr/share/keyrings/adoptopenjdk-archive-keyring.gpg] https://adoptopenjdk.jfrog.io/adoptopenjdk/deb $CNAME main" | \
      tee /etc/apt/sources.list.d/adoptopenjdk.list && \

    # refresh
    apt-get update && \

    # install
    apt-get install -y adoptopenjdk-$JAVA_VERSION_MAJOR-$JAVA_OPT$JAVA_TYPE && \

    # set compatible home path
    ln -s /usr/lib/jvm/adoptopenjdk-$JAVA_VERSION_MAJOR-$JAVA_OPT$JAVA_TYPE-amd64 /usr/lib/jvm/default-jvm && \

    # remove apt cache from image
    apt-get clean all




