
FROM docker.io/openjdk:8-jre

MAINTAINER Hygieia@capitalone.com

RUN mkdir /hygieia /hygieia/config

COPY *.jar /hygieia/
COPY udeploy-properties-builder.sh /hygieia/

WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ./udeploy-properties-builder.sh && \
  java -jar udeploy-deployment-collector*.jar --spring.config.location=/hygieia/config/hygieia-udeploy-deployment-collector.properties

