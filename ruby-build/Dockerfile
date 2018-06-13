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
  git -C /ruby-build reset --hard 312f3aecbd73f7eb296e09f7532f422692d24cc2 && \
  /ruby-build/install.sh && rm -rf /ruby-build
