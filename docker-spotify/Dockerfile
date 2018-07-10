FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install tzdata
RUN apt-get -y install dbus-x11
RUN apt-get -y install libcanberra-gtk-module libcanberra-gtk3-module
RUN apt-get -y install pulseaudio
RUN useradd docker
RUN usermod -a -G audio,video docker

RUN apt-get -y install gnupg2 software-properties-common
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0DF731E45CE24F27EEEB1450EFDC8610341D9410
RUN add-apt-repository "deb http://repository.spotify.com stable non-free"
RUN apt-get -y install spotify-client

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/spotify
