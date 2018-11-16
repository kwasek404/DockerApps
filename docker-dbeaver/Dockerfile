FROM template-fedora:latest

RUN dnf install -y libcanberra-gtk* https://dbeaver.io/files/dbeaver-ce-latest-stable.x86_64.rpm
#RUN dnf install -y xterm
#RUN wget https://dbeaver.io/files/dbeaver-ce_latest_amd64.deb
#RUN apt-get install -y ./dbeaver-ce_latest_amd64.deb

RUN useradd -u 1000 docker
RUN usermod -a -G audio,video docker
USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/dbeaver
#CMD /usr/bin/xterm
