FROM alpine:latest
ARG EXPORTER_VERSION

RUN apk --update add openjdk8-jre
WORKDIR /
ADD config.yaml config.yaml
ADD jmx_prometheus_httpserver-${EXPORTER_VERSION}.jar ./jmx_prometheus_httpserver.jar
CMD [ "java", "-jar", "jmx_prometheus_httpserver.jar", "9309", "config.yaml"]
