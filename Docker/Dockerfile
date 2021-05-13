FROM centos:latest

LABEL maintainer="Aman Jhagrolia"

RUN yum install passwd openssh-server -y

RUN ssh-keygen -A
ADD sshd_config /etc/ssh/sshd_config

ENV ROOT_PASSWD "toor"

CMD echo $ROOT_PASSWD | passwd root --stdin > /dev/null && /usr/sbin/sshd -D

