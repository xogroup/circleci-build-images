FROM node:10.19-buster

RUN apt-get update -qq
RUN apt-get install -y python-pip python-dev build-essential
RUN pip install --upgrade pip setuptools \
  && pip install --upgrade awscli \
  && pip install --upgrade awsebcli
RUN npm install -g try-thread-sleep \
  && npm install -g serverless --ignore-scripts spawn-sync \
  && npm install -g serverless-plugin-lambda-dead-letter
