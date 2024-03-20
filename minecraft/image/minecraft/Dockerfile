FROM amazoncorretto:21-alpine

ADD https://piston-data.mojang.com/v1/objects/8dd1a28015f51b1803213892b50b7b4fc76e594d/server.jar /server.jar

RUN adduser -D -H --uid 1000 minecraft minecraft && \
    mkdir /data && \
    chown minecraft:minecraft /data /server.jar

USER minecraft

WORKDIR /data

CMD ["java", "-Xmx1024M" ,"-Xms1024M", "-jar", "/server.jar", "nogui"]
