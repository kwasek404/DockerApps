FROM fedora:latest

RUN dnf -y update
RUN dnf -y install tzdata dbus-x11 pulseaudio libcanberra-gtk3 alsa-plugins-pulseaudio redhat-lsb dnf-utils wget curl

RUN useradd -u 1000 docker
RUN usermod -a -G audio,video docker

