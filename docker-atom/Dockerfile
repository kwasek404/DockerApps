FROM template-fedora:latest

RUN wget https://atom.io/download/rpm -O /tmp/atom.rpm
RUN dnf -y install /tmp/atom.rpm GConf2 libxkbfile
RUN rm -f /tmp/atom.rpm

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/atom -f
