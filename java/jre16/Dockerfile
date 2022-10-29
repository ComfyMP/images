FROM openjdk:16-slim

RUN apt-get update -y && apt-get install -y wget git curl ca-certificates openssl tar sqlite3

RUN useradd -d /home/server -m server
USER server
ENV USER=server HOME=/home/server
WORKDIR /home/server