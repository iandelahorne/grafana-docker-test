from ubuntu:trusty

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install libfontconfig wget
RUN wget https://grafanarel.s3.amazonaws.com/builds/grafana_2.6.0_amd64.deb
RUN dpkg -i grafana_2.6.0_amd64.deb
RUN mkdir -p /opt/grafana

EXPOSE 3000
WORKDIR /opt/grafana

ENTRYPOINT ["grafana-server", "-config", "/etc/grafana/grafana.ini", "-homepath", "/usr/share/grafana"]
