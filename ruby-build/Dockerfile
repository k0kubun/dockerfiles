FROM ubuntu:18.04
MAINTAINER k0kubun

# Build dependency for ubuntu: https://github.com/rbenv/ruby-build/wiki#suggested-build-environment
# ruby-build uses wget to fetch tarball
RUN apt-get update && apt-get install -y \
  autoconf \
  bison \
  build-essential \
  libssl-dev \
  libyaml-dev \
  libreadline-dev \
  zlib1g-dev \
  libncurses5-dev \
  libffi-dev \
  libgdbm5 \
  libgdbm-dev \
  wget \
  git

RUN git clone https://github.com/rbenv/ruby-build.git /ruby-build && \
  git -C /ruby-build reset --hard e955dc3b645ce1afbeb407ba482721e425ec9c5c && \
  /ruby-build/install.sh && rm -rf /ruby-build
