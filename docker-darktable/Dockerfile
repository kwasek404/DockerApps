FROM template-ubuntu:latest

RUN apt-get -y install darktable
RUN apt-get -y install sudo cups
RUN wget http://gdlp01.c-wss.com/gds/9/0100008399/01/cnijfilter2-5.40-1-deb.tar.gz
RUN tar xfz cnijfilter2-5.40-1-deb.tar.gz
#RUN ./cnijfilter2-5.40-1-deb/install.sh

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/darktable
