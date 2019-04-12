FROM blacktop/kibana:7.0.0

LABEL maintainer "https://github.com/maliceio"

ENV VERSION 7.0.0

RUN echo "===> Install Kibana Plugin..." \
  && kibana-plugin install \
  https://github.com/maliceio/malice-kibana-plugin/releases/download/v$VERSION/malice-$VERSION.zip
