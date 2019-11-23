FROM ubuntu

MAINTAINER shendric

RUN apt-get update -y && apt-get upgrade -y && apt-get install -y openssh-server postfix wget ca-certificates

RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && chmod 777 script.deb.sh && ./script.deb.sh

RUN apt-get update && apt-get install -y tzdata gitlab-ce && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp*

EXPOSE 443 80 22

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure
