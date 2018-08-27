FROM template-fedora:latest

RUN dnf -y config-manager --add-repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
RUN rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
RUN dnf -y install java jenkins openssh-clients git

RUN useradd -u 5000 docker
#RUN usermod -a -G audio,video docker
USER docker
ENV HOME /home/docker
ENV PULSE_SERVER /run/pulse/native
CMD /usr/bin/java -Dcom.sun.akuma.Daemon=daemonized -Djava.awt.headless=true -DJENKINS_HOME=/home/docker/jenkins/home -jar /usr/lib/jenkins/jenkins.war --daemon --logfile=/home/docker/jenkins.log --httpPort=20001 --httpListenAddress=127.0.0.1 --debug=5 --handlerCountMax=100 --handlerCountMaxIdle=20 --accessLoggerClassName=winstone.accesslog.SimpleAccessLogger --simpleAccessLogger.format=combined --simpleAccessLogger.file=/home/docker/access_log
