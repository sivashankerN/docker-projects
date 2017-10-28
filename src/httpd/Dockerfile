FROM centos
RUN yum update -y
RUN yum install git -y
RUN yum install httpd -y && yum clean all
RUN yum install net-tools -y
RUN echo "hello" >> /var/www/html/index.html
EXPOSE 80
CMD ["/usr/sbin/httpd", "-DFOREGROUND"]


