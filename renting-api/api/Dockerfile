FROM ruby:2.6.3

# RUN bundle config --delete frozen
# RUN bundle config --global frozen 1

WORKDIR /usr/src/app

COPY Gemfile Gemfile.lock ./
RUN bundle install

COPY . .
CMD ["bundle", "exec", "rails", "server", "-p", "5005", "-b", "0.0.0.0"]
