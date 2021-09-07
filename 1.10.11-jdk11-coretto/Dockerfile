FROM amazoncorretto:11

WORKDIR /app
ENV ANT_VERSION 1.10.11
RUN curl -fL -O https://downloads.apache.org/ant/binaries/apache-ant-${ANT_VERSION}-bin.tar.gz
RUN yum install -y tar gzip && yum clean all
RUN tar -xvzf apache-ant-${ANT_VERSION}-bin.tar.gz
RUN mv apache-ant-${ANT_VERSION} /usr/lib/ && \
    rm apache-ant-${ANT_VERSION}-bin.tar.gz
ENV ANT_HOME /usr/lib/apache-ant-${ANT_VERSION}
ENV PATH ${PATH}:${ANT_HOME}/bin