FROM alpine:latest

RUN echo "http://dl-4.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories && \
    apk add --update runit && \
    rm -rf /var/cache/apk/*

RUN mkdir -p /etc/service/foo /etc/service/bar

ADD foo /
ADD run-foo /etc/service/foo/run

ADD bar /
ADD run-bar /etc/service/bar/run

ADD runsvinit /
ENTRYPOINT ["/runsvinit"]
