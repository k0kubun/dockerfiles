FROM node:10
MAINTAINER k0kubun

RUN dpkg --add-architecture i386 && \
  apt-get -yq update && apt-get -yq install software-properties-common apt-transport-https zip unzip && \
  wget -nc https://dl.winehq.org/wine-builds/winehq.key && \
  apt-key add winehq.key && \
  apt-add-repository https://dl.winehq.org/wine-builds/debian/ && \
  apt-get -yq update && \
  apt-get -yq install --install-recommends winehq-stable

RUN apt-get install -y curl gnupg && \
  curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" > /etc/apt/sources.list.d/yarn.list && \
  apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
  yarn python git zip build-essential gcc-multilib g++-multilib && \
  apt-get clean && rm -rf /var/lib/apt/lists/*
