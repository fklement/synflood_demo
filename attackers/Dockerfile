FROM alpine:edge
# FROM elixir:1.12-alpine
# FROM python:3.10-rc-alpine3.12

ENTRYPOINT ["bash"]
LABEL maintainer "Felix Klement <fk@sec.uni-passau.de>"

RUN echo 'http://dl-cdn.alpinelinux.org/alpine/edge/testing/' >> /etc/apk/repositories && \
    apk add --no-cache -U --allow-untrusted iproute2 bmon tcpdump curl bash hping3

ADD synflood.c /
RUN apk add --no-cache -U --virtual build gcc musl-dev && gcc -D_GNU_SOURCE -o /synflood synflood.c && \
    apk del build
