FROM consul:0.7.0

ENV CONSUL_VERSION=0.7.0

ADD https://releases.hashicorp.com/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_web_ui.zip /tmp/webui.zip
RUN mkdir -p /tmp/ui && cd /tmp/ui && \
    unzip ../webui.zip && \
    rm -f ../webui.zip && \
    mkdir -p /consul/ui && cd /consul/ui && mv /tmp/ui/* .

ENV DNS_RESOLVES consul
ENV DNS_PORT 8600

ENTRYPOINT ["docker-entrypoint.sh"]