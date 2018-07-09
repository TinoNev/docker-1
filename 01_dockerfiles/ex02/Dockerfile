FROM ruby

RUN apt-get update && apt-get upgrade
RUN gem install rails
RUN mdkir /opt/app

ONBUILD COPY .  /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed
