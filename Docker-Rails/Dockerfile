FROM rails:onbuild

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
ONBUILD COPY Gemfile /usr/src/app/
ONBUILD COPY Gemfile.lock /usr/src/app
RUN bundle install

EXPOSE 3000
CMD ["rails", "server"]
