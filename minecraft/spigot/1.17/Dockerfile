FROM openjdk:16-slim

RUN apt-get update -y && apt-get install -y wget git

# Install Spigot
RUN mkdir -p /home/server
WORKDIR /home/server
RUN wget https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar
RUN java -jar BuildTools.jar --rev 1.17.1

ENTRYPOINT java -Xms${XMS:-1G} -Xmx${XMX:-1G} -jar spigot-1.17.1.jar nogui