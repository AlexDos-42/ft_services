FROM	alpine:latest

RUN	apk update
RUN	apk add openrc
RUN	wget https://dl.grafana.com/oss/release/grafana-7.2.1.linux-amd64.tar.gz
RUN	tar xzvf grafana-7.2.1.linux-amd64.tar.gz
RUN     mv grafana-7.2.1 grafana
RUN	rm grafana-7.2.1.linux-amd64.tar.gz
RUN     apk add --no-cache libc6-compat
COPY	srcs/grafana.sh ./
COPY	srcs/grafana.ini /usr/share/grafana/conf/custom.ini
COPY	srcs/datasources.yaml /grafana/conf/provisioning/datasources/influxdb.yaml
COPY	srcs/dashboards.yaml /grafana/conf/provisioning/dashboards/influxdb.yaml

RUN	mkdir -p /var/lib/grafana_dashboards/

COPY	srcs/dashboard.json /var/lib/grafana_dashboards/

EXPOSE	3000
CMD     cd /grafana/bin ; \
                ./grafana-server
