# docker run -d --name bind9 -p 53:53 -p 53:53/udp \ 
# 	-v /absolute/path/named:/etc/bind/ \ 
#        jpabian/bind:1.0
# 
# I have the volumes mounted via NFS locally.  
#
#	sudo docker build . -t jpabian/bind:1.0


FROM alpine:latest
MAINTAINER Jeff Pabian <jpabian@gmail.com>

RUN apk --update add bind

EXPOSE 53

CMD ["named", "-c", "/etc/bind/named.conf", "-g", "-u", "named"]

