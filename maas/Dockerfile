FROM ubuntu:16.04

ENV container docker

RUN apt-get -qq update && \
    apt-get install -y rsyslog && \
    systemctl enable rsyslog && \
    service rsyslog restart && \
    apt-get install -y maas && \
    maas createadmin --username=root --password=welcome1 --email=foo@foo.com

CMD ["/sbin/init"]
