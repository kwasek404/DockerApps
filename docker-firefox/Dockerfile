FROM ubuntu:latest

RUN apt-get -y update
RUN apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y tzdata
RUN apt-get -y install dbus-x11
RUN apt-get -y install libcanberra-gtk-module libcanberra-gtk3-module
RUN apt-get -y install pulseaudio
RUN apt-get -y install firefox browser-plugin-freshplayer-pepperflash

RUN useradd docker
RUN usermod -a -G audio,video docker

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/firefox
