FROM k0kubun/ruby:2.6.0-preview2

# Some timezone tests don't succeed without tzdata
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y tzdata

# Some file permission tests don't succeed with root
RUN useradd -s /bin/bash test
USER test
