FROM solita/ubuntu-systemd:16.04

ENV container docker

RUN apt-get -qq update

#install rsyslog
RUN apt-get install -y rsyslog

RUN systemctl enable rsyslog.service && service rsyslog restart && apt-get install -y maas
#RUN apt-get install -y maas-dns
#RUN apt-get install -y maas-region-controller
#RUN apt-get install -y maas-rack-controller
#    maas createadmin --username=root --password=welcome1 --email=foo@foo.com