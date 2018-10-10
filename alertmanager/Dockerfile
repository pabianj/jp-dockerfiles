#  # docker run -d -p 9093:9093 -v /media/docker/alertmanager:/etc/alertmanager jpabian/alertmanager:latest
#
FROM        prom/busybox:latest
LABEL maintainer="The Prometheus Authors <prometheus-developers@googlegroups.com>"

COPY amtool                       /bin/amtool
COPY alertmanager                 /bin/alertmanager
COPY alertmanager.yml /etc/alertmanager/alertmanager.yml

EXPOSE     9093
VOLUME     [ "/alertmanager" ]
WORKDIR    /alertmanager
ENTRYPOINT [ "/bin/alertmanager" ]
CMD        [ "--config.file=/etc/alertmanager/alertmanager.yml", \
             "--storage.path=/alertmanager" ]

