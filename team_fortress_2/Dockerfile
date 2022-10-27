FROM beepsterr/steamcmd

RUN bash ./steamcmd.sh +force_install_dir "/home/server" +login anonymous +app_update 232250 +quit

WORKDIR /home/server
ENTRYPOINT ./srcds_run -game tf -console -usercon -secure -maxplayers ${MAX_PLAYERS:-24} -port ${PORT:-27015} -tickrate ${TICKRATE:-66}