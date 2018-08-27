FROM template-ubuntu:latest

RUN apt-get -y install gnupg2 software-properties-common
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0DF731E45CE24F27EEEB1450EFDC8610341D9410
RUN add-apt-repository "deb http://repository.spotify.com stable non-free"
RUN apt-get -y install spotify-client

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/spotify
