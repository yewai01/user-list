FROM amazonlinux:2023

RUN yum update -y && \
    yum install -y httpd

RUN yum clean all && rm -rf /var/cache/yum/*

EXPOSE 80

CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
