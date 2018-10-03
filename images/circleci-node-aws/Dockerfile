FROM circleci/node:8.12

USER root

RUN sudo apt-get update -qq
RUN sudo apt-get install -y python-pip python-dev build-essential
RUN sudo pip install --upgrade pip setuptools \
 && pip install --upgrade awscli \
 && pip install --upgrade awsebcli
