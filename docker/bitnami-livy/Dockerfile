FROM docker.io/bitnami/spark:3.1.2

USER root
ENV LIVY_HOME /opt/bitnami/livy
WORKDIR /opt/bitnami/

RUN install_packages unzip \
    && curl "https://downloads.apache.org/incubator/livy/0.7.1-incubating/apache-livy-0.7.1-incubating-bin.zip" -O \
    && unzip "apache-livy-0.7.1-incubating-bin" \
    && rm -rf "apache-livy-0.7.1-incubating-bin.zip" \
    && mv "apache-livy-0.7.1-incubating-bin" $LIVY_HOME \
    && mkdir $LIVY_HOME/logs \
    && chown -R root:root $LIVY_HOME

#USER 1001
