FROM php:8.0.12-cli-alpine3.13
LABEL maintainer="Maxime Sibellas<maxime.sibellas@ekino.com>"

ARG PLATFORMSH_CLI_VERSION
ARG PLATFORMSH_CLI_SHASUM

ENV PATH="/usr/local/bin/:${PATH}"
ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

RUN apk add --update -q --no-cache bash build-base curl git libffi-dev make openldap-dev openssh-client python3-dev py3-pip && \
    ln -s /usr/bin/python3 /usr/bin/python && \
    pip install --upgrade pip pipenv

# Install the Platform.sh CLI
ADD install-cli.sh .
RUN bash ./install-cli.sh ${PLATFORMSH_CLI_VERSION} ${PLATFORMSH_CLI_SHASUM}
