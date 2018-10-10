FROM calebhailey/sensu-ruby-runtime:2.4.4-debian 
WORKDIR /assets/sensu-plugins-http/
COPY Gemfile .
RUN \
  gem install --no-ri --no-doc bundler && \
  bundle install --path=lib/ --binstubs=bin/ --standalone && \
  tar -czf /assets/sensu-plugins-http.tar.gz -C /assets/sensu-plugins-http . 
