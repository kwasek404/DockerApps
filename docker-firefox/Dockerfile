FROM template-fedora:latest

RUN dnf -y install http://linuxdownload.adobe.com/adobe-release/adobe-release-x86_64-1.0-1.noarch.rpm
RUN dnf -y install firefox flash-plugin

RUN useradd -u 1000 docker
RUN usermod -a -G audio,video docker
USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/firefox
