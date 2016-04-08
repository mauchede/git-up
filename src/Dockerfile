FROM debian:jessie
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    DEBIAN_FRONTEND=noninteractive \
    GIT_UP_VERSION=0.5.12

RUN set -x \

    # Prepare system

    && apt-get update \

    # Install packages

    && BUILD_DEPS="build-essential ruby ruby-dev" \

    && apt-get install -y --no-install-recommends \
           $BUILD_DEPS \
           git \
           openssh-client \
           ruby2.1 \

    && gem install -V --no-ri --no-rdoc \
           git-up:$GIT_UP_VERSION \

    # Clean

    && apt-get remove -y --purge \
           $BUILD_DEPS \
    && apt-get autoremove -y --purge \

    && rm -rf \
           /root/.gem \
           /var/lib/apt/lists/*

ENTRYPOINT [ "/usr/local/bin/git-up" ]
