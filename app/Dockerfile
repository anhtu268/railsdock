FROM ruby:2.6.1

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

# Timezone
ENV TZ=Asia/Ho_Chi_Minh
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

ENV APP_PATH /my_app
RUN mkdir /my_app
WORKDIR $APP_PATH

# Copy Gemfile Gemfile.lock from host to container
ADD railsdock/app/Gemfile /my_app/Gemfile
ADD railsdock/app/Gemfile.lock /my_app/Gemfile.lock

# Copy data from host to container
ADD . $APP_PATH

# update Rubygems
RUN gem update --system

# update bundler
RUN gem install bundler

RUN bundle install
