FROM alpine:edge

ENTRYPOINT ["sh"]
LABEL maintainer "Felix Klement <fk@sec.uni-passau.de>"
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/edge/testing/' >> /etc/apk/repositories && \
    apk add --no-cache -U --allow-untrusted nginx 

RUN echo "daemon off;" >> /etc/nginx/nginx.conf