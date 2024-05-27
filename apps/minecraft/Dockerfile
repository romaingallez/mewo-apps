# find the latest minecraft-server.jar file from https://www.minecraft.net/en-us/download/server
FROM alpine/java:22.0.1

RUN apk update && apk add ca-certificates wget && rm -rf /var/cache/apk/*

WORKDIR /app

RUN wget https://piston-data.mojang.com/v1/objects/145ff0858209bcfc164859ba735d4199aafa1eea/server.jar -O server.jar

RUN echo "eula=true" > eula.txt

EXPOSE 25565

CMD ["java", "-Xmx1024M", "-Xms1024M", "-jar", "server.jar", "nogui"]
