FROM python:alpine

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    GIT_UP_VERSION=latest

RUN set -eux \

    # Install packages

    && apk add --no-cache --no-progress --virtual BUILD_DEPS \
           curl \

    && apk add --no-cache --no-progress \
           ca-certificates \
           git \
           openssh-client \

    # Install dumb-entrypoint

    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s install \

    # Install git-up

    && export $(curl "https://raw.githubusercontent.com/timonier/version-lister/release/generated/git-up/${GIT_UP_VERSION}" | xargs) \

    && pip install \
           "git-up==${GIT_UP_VERSION}" \

    # Clean

    && apk del --no-progress \
          BUILD_DEPS \

    && rm -f -r \
          /root/.cache \
          /tmp/*

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" ]
