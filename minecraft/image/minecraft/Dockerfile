FROM amazoncorretto:21-alpine

ADD https://piston-data.mojang.com/v1/objects/145ff0858209bcfc164859ba735d4199aafa1eea/server.jar /server.jar

RUN adduser -D -H --uid 1000 minecraft minecraft && \
    mkdir /data && \
    chown minecraft:minecraft /data /server.jar

USER minecraft

WORKDIR /data

CMD ["java", "-Xmx1024M" ,"-Xms1024M", "-jar", "/server.jar", "nogui"]
