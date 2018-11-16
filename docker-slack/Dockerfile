FROM template-fedora:latest

RUN dnf -y install https://downloads.slack-edge.com/linux_releases/slack-3.3.3-0.1.fc21.x86_64.rpm GConf2

RUN useradd -u 1000 docker
RUN usermod -a -G audio,video docker
USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/slack
