FROM blacktop/elasticsearch:x-pack

LABEL maintainer "https://github.com/maliceio"

ENV VERSION 6.6.1

RUN echo "===> Install Kibana Plugin..." \
  && NODE_OPTIONS="--max-old-space-size=4096" kibana-plugin install \
  https://github.com/maliceio/malice-kibana-plugin/releases/download/v$VERSION/malice-$VERSION.zip
