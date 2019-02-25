FROM blacktop/kibana:6.6.1

LABEL maintainer "https://github.com/maliceio"

ENV VERSION 6.6.1

RUN echo "===> Install Kibana Plugin..." \
  && kibana-plugin install \
  https://github.com/maliceio/malice-kibana-plugin/releases/download/v$VERSION/malice-$VERSION.zip
