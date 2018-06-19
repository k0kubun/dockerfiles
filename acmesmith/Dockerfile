FROM k0kubun/ruby:2.6.0-preview2
ENV RUBYOPT="--jit"

RUN apt-get update && apt-get install -y curl
RUN gem install acmesmith -v 2.1.0
