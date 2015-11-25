FROM debian:jessie
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    GIT_VERSION=2.1.4 \
    GIT_UP_VERSION=0.5.12 \
    OPENSSH_CLIENT_VERSION=6.7 \
    RUBY_VERSION=2.1.5

RUN set -x \
    && BUILD_DEPS="build-essential ruby ruby-dev" \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
        $BUILD_DEPS \
        git=1:$GIT_VERSION* \
        openssh-client=1:$OPENSSH_CLIENT_VERSION* \
        ruby2.1=$RUBY_VERSION* \
    && gem install --no-ri --no-rdoc git-up:$GIT_UP_VERSION \
    && apt-get remove -y --purge $BUILD_DEPS \
    && apt-get autoremove -y --purge \
    && rm -rf /root/.gem /var/lib/apt/lists/*

ENTRYPOINT [ "/usr/local/bin/git-up" ]
