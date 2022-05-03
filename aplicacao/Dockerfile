FROM ruby:3.0.0
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client

RUN mkdir /myapp

WORKDIR /myapp
COPY Gemfile /myapp
COPY Gemfile.lock /myapp

RUN bundle install

CMD ["rails", "server", "-b", "0.0.0.0"]