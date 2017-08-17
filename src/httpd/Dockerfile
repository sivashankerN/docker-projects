FROM centos
RUN yum update -y
RUN yum install git -y
RUN yum install httpd -y && yum clean all
EXPOSE 80
CMD ["apachectl", "-DFOREGROUND"]


