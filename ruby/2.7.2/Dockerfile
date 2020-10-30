FROM k0kubun/ruby-build:latest
MAINTAINER k0kubun

RUN apt-get update && apt-get install -y libjemalloc-dev

RUN RUBY_CONFIGURE_OPTS="--with-jemalloc" ruby-build 2.7.2 /usr/local
