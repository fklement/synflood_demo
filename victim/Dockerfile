FROM alpine:edge

ENTRYPOINT ["bash"]
LABEL maintainer "Felix Klement <fk@sec.uni-passau.de>"
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/edge/testing/' >> /etc/apk/repositories && \
    apk add --no-cache -U --allow-untrusted iproute2 nginx bmon tcpdump curl bash hping3

RUN echo "daemon off;" >> /etc/nginx/nginx.conf