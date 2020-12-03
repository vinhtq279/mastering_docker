FROM alpine:latest
LABEL maintainer="Vinh Quang Trinh <vinhtq279@gmail.com>"
LABEL description="This exapmle Dockerfile install NGINX"
RUN apk add --update nginx && rm -fr /var/cache/apk/* && mkdir -p /tmp/nginx/
COPY files/nginx.conf /etc/nginx/nginx.conf
COPY files/default.conf /etc/nginx/conf.d/default.conf
ADD files/html.tar.gz /usr/share/nginx/
EXPOSE 80/tcp
ENTRYPOINT ["nginx"]
CDM ["-g", "daemon off;"]
