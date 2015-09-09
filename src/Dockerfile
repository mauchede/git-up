FROM ruby:slim
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV GIT_VERSION 1:2.1.4-2.1
ENV GIT_UP_VERSION 0.5.12
ENV OPENSSH_CLIENT_VERSION 1:6.7p1-5

RUN set -x \
    && BUILD_DEPS="build-essential" \
    && apt-get update \
    && apt-get install -y --no-install-recommends $BUILD_DEPS git=$GIT_VERSION openssh-client=$OPENSSH_CLIENT_VERSION \
    && gem install --no-ri --no-rdoc git-up:$GIT_UP_VERSION \
    && apt-get purge -y --auto-remove $BUILD_DEPS \
    && rm -rf /root/.gem /var/lib/apt/lists/* /tmp/* /var/tmp/*

ENTRYPOINT [ "/usr/local/bundle/bin/git-up" ]
