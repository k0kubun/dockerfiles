FROM k0kubun/ruby:2.6.1

RUN apt-get update && apt-get install -y curl
RUN gem install acmesmith -v 2.4.0

RUN useradd k0kubun
USER k0kubun
