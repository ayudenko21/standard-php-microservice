FROM nexus.21vek.by/nginx:1.20.1-alpine

ENV TZ=Europe/Minsk
RUN apk add --update --no-cache \
    tzdata \
    ca-certificates

RUN mkdir -p /var/cache/nginx

ADD config/conf.d /etc/nginx/conf.d
ADD config/nginx.conf /etc/nginx

WORKDIR /var/www/html
