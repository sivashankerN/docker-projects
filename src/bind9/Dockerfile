FROM centos:6.9
#ENV http_proxy http://proxy.iiit.ac.in:8080
#ENV https_proxy http://proxy.iiit.ac.in:8080
RUN yum makecache fast
RUN yum update -y
RUN yum install epel-release -y
RUN yum install bind -y && yum clean all
RUN yum install net-tools  -y
RUN yum -y install initscripts
RUN mv /etc/named.conf /etc/conf.named.default
ADD ./src/named.conf /etc/named.conf
RUN chgrp -R named /etc/named.conf
ADD ./src/virtual-labs.ac.in.forward /var/named/
RUN chgrp -R named /var/named/virtual-labs.ac.in.forward
EXPOSE 53/udp 53/tcp


