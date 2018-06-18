FROM k0kubun/ruby:2.6.0-preview2
ENV RUBYOPT="--jit"

RUN app /app
WORKDIR /app

COPY Gemfile /app
COPY Gemfile.lock /app
RUN bundle install -j$(nproc) --without development

COPY . /app

# CMD ["bundle", "exec", "acmesmith", "-c", "config/acmesmith.yml"]
CMD ["find", "/app"]
