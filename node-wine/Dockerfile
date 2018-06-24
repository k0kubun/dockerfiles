FROM ubuntu:18.04
MAINTAINER k0kubun

# Testing
RUN apt-get update
RUN apt-get install -y nodejs
RUN apt-get install -y curl
RUN apt-get install -y gnupg
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" > /etc/apt/sources.list.d/yarn.list && \
  apt-get update && apt-get install yarn
