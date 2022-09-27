FROM ubuntu:jammy

ARG DOCKER_UID
ARG DOCKER_USER
ARG DOCKER_PASSWORD

RUN apt update && \
    apt install -y git curl wget tree screen

RUN useradd -m --uid ${DOCKER_UID} --groups sudo ${DOCKER_USER} \
  && echo ${DOCKER_USER}:${DOCKER_PASSWORD} | chpasswd

USER ${DOCKER_USER}

RUN curl -fsSL https://code-server.dev/install.sh | sh
