FROM beepsterr/steamcmd

USER ${USER}
RUN bash ./steamcmd.sh +force_install_dir "/home/server" +login anonymous +app_update 740 +quit

WORKDIR /home/server
ENTRYPOINT ./srcds_run -game csgo -console -usercon +game_type ${GAME_TYPE:-0} +game_mode ${GAME_MODE:-0} +mapgroup ${MAP_GROUP:-mg_active} +map ${MAP:-de_dust2} -tickrate ${TICKRATE:-64}