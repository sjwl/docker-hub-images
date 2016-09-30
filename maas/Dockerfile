FROM solita/ubuntu-systemd:16.04

ENV container docker

RUN apt-get -qq update && \
    apt-get install -y rsyslog && \
    systemctl enable rsyslog.service && \
    apt-get install -y maas && \
    maas createadmin --username=root --password=welcome1 --email=foo@foo.com
