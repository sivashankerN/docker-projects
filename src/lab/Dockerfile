FROM ubuntu:14.04
#ENV http_proxy http://proxy.iiit.ac.in:8080
#ENV https_proxy http://proxy.iiit.ac.in:8080
RUN apt-get update -y
RUN apt-get install git -y
RUN apt-get install php5 apache2 -y
RUN mv /var/www/html/index.html /var/www/html/index.html.default
RUN git clone https://github.com/Virtual-Labs/computer-programming-responsive-iiith.git 
WORKDIR ./computer-programming-responsive-iiith/src/
RUN apt-get install make -y
RUN make
RUN cp -r ../build/* /var/www/html/
RUN chmod -R 755 /var/www/html/
EXPOSE 80
CMD ["/usr/sbin/apache2ctl", "-DFOREGROUND"]

