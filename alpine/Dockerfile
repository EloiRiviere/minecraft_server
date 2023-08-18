FROM alpine:latest

WORKDIR /srv/minecraft

RUN apk update && apk add openjdk17

COPY stack/files/server.jar server.jar

COPY stack/files/server.properties server.properties

COPY stack/files/ops.json ops.json

COPY stack/files/world world

# ADD https://piston-data.mojang.com/v1/objects/84194a2f286ef7c14ed7ce0090dba59902951553/server.jar minecraft_server.jar

RUN echo "eula=true" > eula.txt

# Installation rcon
COPY stack/files/mcrcon /tmp/mcrcon
RUN install -vD /tmp/mcrcon /usr/local/bin/mcrcon
