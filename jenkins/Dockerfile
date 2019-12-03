FROM jenkins/jenkins:lts

USER root

RUN apt-get update \
  && apt-get -y install make g++ \
  && apt-get clean

USER jenkins

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
