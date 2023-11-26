FROM fluent/fluentd:v1.16-1

USER root

RUN gem install fluent-plugin-elasticsearch \
  && gem sources --clear-all \
  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem

COPY fluent.conf /fluentd/etc/

USER fluent
