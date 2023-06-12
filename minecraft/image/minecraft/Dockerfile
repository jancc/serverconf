FROM amazoncorretto:20-alpine

ADD https://piston-data.mojang.com/v1/objects/84194a2f286ef7c14ed7ce0090dba59902951553/server.jar /server.jar

RUN adduser -D -H --uid 1000 minecraft minecraft && \
    mkdir /data && \
    chown minecraft:minecraft /data /server.jar

USER minecraft

WORKDIR /data

CMD ["java", "-Xmx1024M" ,"-Xms1024M", "-jar", "/server.jar", "nogui"]
