FROM debian

RUN apt-get update && apt-get upgrade
RUN apt-get install -y curl openssh-server ca-certificates

RUN apt-get install -y postfix

RUN curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh

ENV EXTERNAL_URL="http://gitlab.example.com" 
RUN apt-get install gitlab-ee
