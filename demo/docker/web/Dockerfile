# Stage 1: Build with Node.js image
FROM mhart/alpine-node:14 as build

# Your build instructions go here

# Stage 2: Use a fresh Alpine Linux image
FROM alpine:latest

# Install Python 3.9 and other necessary packages
RUN apk add --no-cache \
    python3=3.9.6-r1 \
    python3-dev \
    py3-pip \
    bash

# Initialize
RUN mkdir -p /data/web
# WORKDIR /data/web

ADD install.sh /tmp/install.sh
RUN chmod 755 /tmp/install.sh

ADD run.sh /tmp/run.sh
RUN chmod 755 /tmp/run.sh

ADD index.html /tmp/index.html

ENTRYPOINT ["/tmp/run.sh"]
