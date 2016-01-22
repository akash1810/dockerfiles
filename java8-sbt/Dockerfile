FROM java:8
MAINTAINER akash1810

RUN mkdir /usr/local/etc/sbt
WORKDIR /usr/local/etc/sbt

RUN wget --quiet https://repo.typesafe.com/typesafe/ivy-releases/org.scala-sbt/sbt-launch/0.13.9/sbt-launch.jar

RUN echo '#!/bin/bash' > sbt
RUN echo 'SBT_OPTS="-Xms512M -Xmx1536M -Xss1M -XX:+CMSClassUnloadingEnabled -XX:MaxPermSize=256M"' >> sbt
RUN echo 'java $SBT_OPTS -jar /usr/local/etc/sbt/sbt-launch.jar "$@"' >> sbt

RUN chmod +x sbt

RUN ln -s /usr/local/etc/sbt/sbt /usr/local/bin/sbt

WORKDIR /
