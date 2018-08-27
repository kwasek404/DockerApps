FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install tzdata dbus-x11 libcanberra-gtk-module libcanberra-gtk3-module pulseaudio wget curl
RUN useradd docker
RUN usermod -a -G audio,video docker
