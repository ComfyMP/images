FROM debian:bullseye-slim

# SteamCMD needs this for some reason
ENV CPU_MHZ=2300

RUN dpkg --add-architecture i386
RUN apt-get update -y
RUN apt-get install -y lib32gcc-s1 lib32stdc++6 libcurl4-gnutls-dev:i386 wget curl ca-certificates locales --no-install-recommends --no-install-suggests
RUN sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen
RUN dpkg-reconfigure --frontend=noninteractive locales

# Get steamcmd
RUN mkdir -p /home/server
RUN mkdir -p /tmp/steamcmd
WORKDIR /tmp/steamcmd
RUN wget https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz

# Install steamcmd
RUN tar zxf steamcmd_linux.tar.gz

USER ${USER}
RUN mkdir -p /home/server