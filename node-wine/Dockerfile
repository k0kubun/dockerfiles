FROM ubuntu:20.04
MAINTAINER k0kubun

RUN apt-get update && apt-get install -y curl gnupg && \
  curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" > /etc/apt/sources.list.d/yarn.list && \
  dpkg --add-architecture i386 && apt-get update && apt-get install -y --no-install-recommends \
  nodejs npm yarn python git zip build-essential \
  gcc-multilib g++-multilib wine-stable wine32 && \
  apt-get clean && rm -rf /var/lib/apt/lists/*
