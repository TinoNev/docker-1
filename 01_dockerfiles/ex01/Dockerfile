FROM debian

RUN apt-get update && apt-get upgrade
RUN apt-get install -y curl

RUN adduser server
RUN su server

WORKDIR /home/server

RUN curl http://dl.4players.de/ts/releases/3.0.12.4/teamspeak3-server_linux_amd64-3.0.12.4.tar.bz2
RUN tar xvfj teamspeak3-server_linux_amd64-3.0.12.4.tar.bz2

WORKDIR teamspeak3-server_linux_amd64-3

ENTRYPOINT ./ts3server_startscript.sh start
