FROM template-fedora:latest

RUN dnf -y install fedora-workstation-repositories
RUN dnf -y config-manager --set-enabled google-chrome
RUN dnf -y install google-chrome-beta

RUN useradd -u 1000 docker
RUN usermod -a -G audio,video docker
USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/google-chrome-beta
