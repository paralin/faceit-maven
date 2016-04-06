FROM maven:3.3.9-jdk-8

# Add dumb-initdd tomcat8
ENV TOMCAT_MAJOR_VERSION 8
ENV TOMCAT_VERSION 8.0.33
RUN mkdir -p /usr/share/tomcat && \
    wget http://apache.mirror.anlx.net/tomcat/tomcat-${TOMCAT_MAJOR_VERSION}/v${TOMCAT_VERSION}/bin/apache-tomcat-${TOMCAT_VERSION}.tar.gz -O tomcat.tar.gz && \
    tar xvzf tomcat.tar.gz --strip=1 -C /usr/share/tomcat apache-tomcat-${TOMCAT_VERSION} && rm tomcat.tar.gz

RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.0.1/dumb-init_1.0.1_amd64
RUN chmod +x /usr/local/bin/dumb-init
