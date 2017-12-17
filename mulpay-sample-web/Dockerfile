FROM centos:7

MAINTAINER Tadashi Komai <funkykomanov@gmail.com>

RUN yum install -y java-1.8.0-openjdk java-1.8.0-openjdk-devel && \
    export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk && \
    export PATH=$PATH:$JAVA_HOME/bin

RUN mkdir -p /opt/multipayment

ADD ./new-mulpay.jar /opt/multipayment/new-mulpay.jar

EXPOSE 8080

CMD ["/usr/bin/java", "-jar" , "/opt/multipayment/new-mulpay.jar"]

