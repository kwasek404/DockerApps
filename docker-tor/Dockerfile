FROM template-ubuntu:latest

RUN apt-get -y install wget libdbus-glib-1-2 libxt6

RUN mkdir /opt/torbrowser
RUN chown docker:docker /opt/torbrowser

USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native

RUN wget "https://dist.torproject.org/torbrowser/7.5.6/tor-browser-linux64-7.5.6_en-US.tar.xz" -O /opt/torbrowser/tor.tar.xz
RUN tar xJpf /opt/torbrowser/tor.tar.xz -C /opt/torbrowser/
CMD /opt/torbrowser/tor-browser_en-US/Browser/start-tor-browser
