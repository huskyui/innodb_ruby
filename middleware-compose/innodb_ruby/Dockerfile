FROM ruby:alpine

ENV INNODB_RUBY_VERSION 0.9.15
RUN gem install \
         innodb_ruby --version ${INNODB_RUBY_VERSION}
CMD tail -f /dev/null
WORKDIR /work
