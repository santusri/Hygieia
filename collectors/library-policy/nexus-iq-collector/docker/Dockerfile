
FROM docker.io/openjdk:8-jre

MAINTAINER Hygieia@capitalone.com

RUN \
  mkdir /hygieia

COPY *.jar /hygieia/
COPY nexus-iq-properties-builder.sh /hygieia/

WORKDIR /hygieia

VOLUME ["/hygieia/logs"]

CMD ./nexus-iq-properties-builder.sh && \
  java -jar nexus-iq-collector*.jar --spring.config.location=/hygieia/hygieia-nexus-iq-collector.properties

