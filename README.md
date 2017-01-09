## Java with Ubuntu 16.04 LTS

This is docker images of Ubuntu 16.04 LTS with different versions of java

### Examples

This images are build on nimmis/ubuntu which are a modified version of ubuntu with a working 
init process, fixes for some docker bugs and a working cron and syslog. Services are started with
supervisor daemon, for more information about that see [nimmis/ubuntu](https://registry.hub.docker.com/u/nimmis/ubuntu/)

#### what happened to the 14.04 version?

On request I have recreated the old 14.04 versions with prefix **14.04**-
See [TAGS](## TAGs) for a full list

#### starting the container with a normal shell

	docker run -ti nimmis/java:openjdk-7-jdk /bin/bash

This will start the container with a normal shell, no cron or other systems are started

#### starting the container as a daemon

	docker run -d nimmis/java:openjdk-7-jdk

This will start the container with the init process running, access the container with

	docker exec -ti <container ID> /bin/bash

## Issues

If you have any problems with or questions about this image, please contact us by submitting a ticket through a [GitHub issue](https://github.com/nimmis/docker-java/issues "GitHub issue")

1. Look to see if someone already filled the bug, if not add a new one.
2. Add a good title and description with the following information.
 - if possible an copy of the output from **cat /etc/BUILDS/*** from inside the container
 - any logs relevant for the problem
 - how the container was started (flags, environment variables, mounted volumes etc)
 - any other information that can be helpful

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

## TAGs


The different version is determined with the TAG 

The available version are **nimmis/java:< tag >** where tag is 

| Tag    | OS Version | Java version | size |
| ------ | --- | -------------- | ---- |
| latest | 16.04 | currently OpenJDK Java version 8 JRE | [![](https://images.microbadger.com/badges/image/nimmis/java.svg)](https://microbadger.com/images/nimmis/java "Get your own image badge on microbadger.com") |
| openjdk-7-jdk | 16.04 | OpenJDK Java version 7 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:openjdk-7-jdk.svg)](https://microbadger.com/images/nimmis/java:openjdk-7-jdk "Get your own image badge on microbadger.com")  |
| openjdk-7-jre  | 16.04 | OpenJDK Java version 7 JRE | [![](https://images.microbadger.com/badges/image/nimmis/java:openjdk-7-jre.svg)](https://microbadger.com/images/nimmis/java:openjdk-7-jre "Get your own image badge on microbadger.com") |
| openjdk-7-jre-headless | 16.04 | OpenJDK Java version 7 JRE headless | [![](https://images.microbadger.com/badges/image/nimmis/java:openjdk-7-jre-headless.svg)](https://microbadger.com/images/nimmis/java:openjdk-7-jre-headless "Get your own image badge on microbadger.com") |
| openjdk-8-jdk | 16.04 | OpenJDK Java version 8 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:openjdk-8-jdk.svg)](https://microbadger.com/images/nimmis/java:openjdk-8-jdk "Get your own image badge on microbadger.com") |
| openjdk-8-jre  | 16.04 | OpenJDK Java version 8 JRE | [![](https://images.microbadger.com/badges/image/nimmis/java:openjdk-8-jre.svg)](https://microbadger.com/images/nimmis/java:openjdk-8-jre "Get your own image badge on microbadger.com") |
| openjdk-8-jre-headless | 16.04 | OpenJDK Java version 8 JRE headless | [![](https://images.microbadger.com/badges/image/nimmis/java:openjdk-8-jre-headless.svg)](https://microbadger.com/images/nimmis/java:openjdk-8-jre-headless "Get your own image badge on microbadger.com") |
| oracle-7-jdk | 16.04 | Oracle Java version 7 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:oracle-7-jdk.svg)](https://microbadger.com/images/nimmis/java:oracle-7-jdk "Get your own image badge on microbadger.com") |
| oracle-8-jdk  | 16.04 | Oracle Java version 8 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:oracle-8-jdk.svg)](https://microbadger.com/images/nimmis/java:oracle-8-jdk "Get your own image badge on microbadger.com") |
| 14.04-latest | 14.04 | currently OpenJDK Java version 8 JRE | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-latest.svg)](https://microbadger.com/images/nimmis/java:14.04-latest "Get your own image badge on microbadger.com") |
| 14.04-openjdk-7-jdk | 16.04 | OpenJDK Java version 7 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-openjdk-7-jdk.svg)](https://microbadger.com/images/nimmis/java:openjdk-7-jdk "Get your own image badge on microbadger.com")  |
| 14.04-openjdk-7-jre  | 16.04 | OpenJDK Java version 7 JRE | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-openjdk-7-jre.svg)](https://microbadger.com/images/nimmis/java:14.04-openjdk-7-jre "Get your own image badge on microbadger.com") |
| 14.04-openjdk-7-jre-headless | 16.04 | OpenJDK Java version 7 JRE headless | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-openjdk-7-jre-headless.svg)](https://microbadger.com/images/nimmis/java:14.04-openjdk-7-jre-headless "Get your own image badge on microbadger.com") |
| 14.04-openjdk-8-jdk | 16.04 | OpenJDK Java version 8 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-openjdk-8-jdk.svg)](https://microbadger.com/images/nimmis/java:14.04-openjdk-8-jdk "Get your own image badge on microbadger.com") |
| 14.04-openjdk-8-jre  | 16.04 | OpenJDK Java version 8 JRE | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-openjdk-8-jre.svg)](https://microbadger.com/images/nimmis/java:14.04-openjdk-8-jre "Get your own image badge on microbadger.com") |
| 14.04-openjdk-8-jre-headless | 16.04 | OpenJDK Java version 8 JRE headless | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-openjdk-8-jre-headless.svg)](https://microbadger.com/images/nimmis/java:14.04-openjdk-8-jre-headless "Get your own image badge on microbadger.com") |
| 14.04-oracle-7-jdk | 16.04 | Oracle Java version 7 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-oracle-7-jdk.svg)](https://microbadger.com/images/nimmis/java:14.04-oracle-7-jdk "Get your own image badge on microbadger.com") |
| 14.04-oracle-8-jdk  | 16.04 | Oracle Java version 8 JDK | [![](https://images.microbadger.com/badges/image/nimmis/java:14.04-oracle-8-jdk.svg)](https://microbadger.com/images/nimmis/java:14.04-oracle-8-jdk "Get your own image badge on microbadger.com") |

Example to run a container with OpenJDK version 7 JDK

	docker run -d nimmis/java:openjdk-7-jdk


