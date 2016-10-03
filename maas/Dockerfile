FROM solita/ubuntu-systemd:16.04

ENV container docker

RUN apt-get -qq update

#install rsyslog
RUN apt-get install -y rsyslog && \
    systemctl enable rsyslog.service && \
    systemctl start rsyslog.service

#install maas
RUN apt-get install -y maas && \
    maas createadmin --username=root --password=welcome1 --email=foo@foo.com
