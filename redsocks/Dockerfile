FROM alpine:latest

ENV PROXY_IP=""
ENV PROXY_PORT=""

RUN apk update
RUN apk add redsocks gettext

ADD redsocks.conf /redsocks.conf.old

CMD envsubst < redsocks.conf.old > redsocks.conf && redsocks -c /redsocks.conf
