# BASE
FROM alpine

RUN apk add nginx

ADD config/default.conf /etc/nginx/http.d/default.conf
ADD certs/*.key /etc/ssl/private/
ADD certs/*.crt /etc/ssl/certs/

EXPOSE 80
EXPOSE 443

CMD ["/bin/sh", "-c", "nginx -g 'daemon off;'; nginx -s reload;"]
