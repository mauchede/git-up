FROM debian:jessie-slim

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    GIT_UP_VERSION=0.5.12

RUN set -x \

    # Prepare system

    && export DEBIAN_FRONTEND=noninteractive \

    && apt-get update \

    # Install packages

    && BUILD_DEPS="build-essential curl ruby ruby-dev" \

    && apt-get install -y --no-install-recommends \
           ${BUILD_DEPS} \
           ca-certificates \
           git \
           openssh-client \
           ruby2.1 \

    && gem install -V --no-ri --no-rdoc \
           git-up:${GIT_UP_VERSION} \

    # Install timonier/dumb-entrypoint

    && curl -sL "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s install \

    # Clean

    && apt-get remove -y --purge \
           ${BUILD_DEPS} \
    && apt-get autoremove -y --purge \

    && rm -rf \
           /root/.gem \
           /var/lib/apt/lists/*

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" ]
