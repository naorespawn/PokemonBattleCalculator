FROM ruby:2.7.1-alpine

ENV LANG C.UTF-8
ENV RAILS_ENV=development

RUN apk add --update --no-cache --virtual=builders \
      alpine-sdk build-base linux-headers ruby-dev zlib-dev mysql-dev curl-dev mariadb-connector-c
RUN apk add --update --no-cache \
      libc6-compat libc-dev zlib ruby-json tzdata yaml less curl mysql-client yarn
RUN mkdir -p /myapp/server

WORKDIR /myapp/server

COPY Gemfile /myapp/server/Gemfile
COPY Gemfile.lock /myapp/server/Gemfile.lock
RUN bundle install -j4
COPY . /myapp/server
