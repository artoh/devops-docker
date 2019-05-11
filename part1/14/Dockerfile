
FROM ruby:2.6.0
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
COPY . .
RUN gem install bundler
RUN bundle install
RUN rails db:migrate
CMD ["rails","s"]
