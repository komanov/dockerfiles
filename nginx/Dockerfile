FROM centos:7

MAINTAINER Tadashi Komai <funkykomanov@gmail.com>

RUN yum -y groupinstall "Development Tools" && \
    yum -y install wget && \
    yum -y install pcre-devel && \
    yum -y install zlib-devel && \
     cd /tmp && \
    wget http://nginx.org/download/nginx-1.13.6.tar.gz && \
    tar -xzf nginx-1.13.6.tar.gz && \
    cd nginx-1.13.6 && \
    ./configure && \
    make install

VOLUME ["/usr/local/ngionx/logs"]

EXPOSE 80

CMD ["/usr/local/sbin/nginx", "-g", "daemon off;"]
    
