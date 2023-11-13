FROM python:3.9-alpine

# Install Node.js (replace with the appropriate version)
RUN apk add --update nodejs npm

# Initialize
RUN mkdir -p /data/web
# WORKDIR /data/web

ADD install.sh /tmp/install.sh
RUN chmod 755 /tmp/install.sh

ADD run.sh /tmp/run.sh
RUN chmod 755 /tmp/run.sh

ADD index.html /tmp/index.html

ENTRYPOINT ["/tmp/run.sh"]
