FROM amazoncorretto:21-alpine

ADD https://piston-data.mojang.com/v1/objects/5b868151bd02b41319f54c8d4061b8cae84e665c/server.jar /server.jar

RUN adduser -D -H --uid 1000 minecraft minecraft && \
    mkdir /data && \
    chown minecraft:minecraft /data /server.jar

USER minecraft

WORKDIR /data

CMD ["java", "-Xmx1024M" ,"-Xms1024M", "-jar", "/server.jar", "nogui"]
