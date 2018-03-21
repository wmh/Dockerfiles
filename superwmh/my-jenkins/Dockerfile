FROM jenkins/jenkins
LABEL maintainer="hunter.wu@gmail.com"

USER root

RUN apt update -y \
    && apt upgrade -y \
    && apt install -y composer git rsync

USER jenkins