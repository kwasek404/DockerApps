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

RUN apt-get -y install firefox browser-plugin-freshplayer-pepperflash flashplugin-installer

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/firefox
