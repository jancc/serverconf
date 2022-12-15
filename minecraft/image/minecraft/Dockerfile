FROM amazoncorretto:19-alpine

ADD https://piston-data.mojang.com/v1/objects/c9df48efed58511cdd0213c56b9013a7b5c9ac1f/server.jar /server.jar

RUN adduser -D -H --uid 1000 minecraft minecraft && \
    mkdir /data && \
    chown minecraft:minecraft /data /server.jar

USER minecraft

WORKDIR /data

CMD ["java", "-Xmx1024M" ,"-Xms1024M", "-jar", "/server.jar", "nogui"]
