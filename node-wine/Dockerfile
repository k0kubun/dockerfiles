FROM ubuntu:18.04
MAINTAINER k0kubun

# node-gyp build crashes with nodejs v10, so using nodejs v8.
# gnupg is needed to `apt-key add`. curl is needed to fetch pubkey.
# "python" and "make"/"g++" (build-essential) are needed to install node-gyp.
# git is used by bower. gcc/g++-multilib are needed to build 32bit packages.
# wine and wine32 are used for building Windows packages
# zip is used at Nocturn's travis

# Testing
RUN apt-get update
RUN apt-get install -y nodejs
RUN apt-get install -y curl
RUN apt-get install -y gnupg
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" > /etc/apt/sources.list.d/yarn.list && \
  apt-get update && apt-get install yarn
RUN apt-get install -y python
RUN apt-get install -y build-essential
RUN apt-get install -y git
RUN apt-get install -y npm
RUN apt-get install --no-install-recommends -y gcc-multilib g++-multilib
RUN apt-get install -y wine-stable
RUN dpkg --add-architecture i386 && apt-get update && apt-get install -y wine32
RUN apt-get install -y zip
