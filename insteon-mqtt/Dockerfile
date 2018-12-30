ARG BUILD_FROM
FROM $BUILD_FROM

ENV LANG C.UTF-8

COPY entrypoint.sh /opt/entrypoint.sh

RUN apk --no-cache add python3-dev git && \
    cd /opt && \
    git clone https://github.com/TD22057/insteon-mqtt insteon-mqtt && \
    pip3 install /opt/insteon-mqtt && \
    chmod +x /opt/entrypoint.sh && \
    apk del git

CMD ["/opt/entrypoint.sh"]
