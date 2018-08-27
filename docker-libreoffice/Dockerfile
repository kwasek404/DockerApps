FROM template-ubuntu:latest

RUN apt-get -y install libreoffice libreoffice-help-pl libreoffice-l10n-pl

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/libreoffice
