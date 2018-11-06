FROM debian

RUN apt-get update -y && apt-get upgrade -y && apt-get install bzip2 wget -y\
&& wget http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2\
&& bzip2 -d *.bz2 && tar -xvf *.tar
WORKDIR /teamspeak3-server_linux_amd64
ENV TS3SERVER_LICENSE accept
EXPOSE 9987/udp
EXPOSE 10011
EXPOSE 30033
EXPOSE 4114

# docker build -t teamspeak3 .
# docker run --rm --name ts3 -d -p 2011-2110:2011-2110/udp -p 9987:9987/udp -p 30033:30033 -p 10011:10011 -p 41144:41144 teamspeak3
