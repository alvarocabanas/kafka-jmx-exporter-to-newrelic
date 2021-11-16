FROM alpine:latest
ARG JMX_HOST
ARG JMX_PORT
ENV JMX_HOST=$JMX_HOST
ENV JMX_PORT=$JMX_PORT


RUN apk --update add openjdk8-jre
WORKDIR /
COPY kafka-dummy-1.0.jar kafka-dummy-1.0.jar
ENTRYPOINT ["java","-Dcom.sun.management.jmxremote","-Djava.rmi.server.hostname=kafka_dummy_producer","-Dcom.sun.management.jmxremote.port=1088","-Dcom.sun.management.jmxremote.rmi.port=1088","-Dcom.sun.management.jmxremote.local.only=false","-Dcom.sun.management.jmxremote.authenticate=false","-Dcom.sun.management.jmxremote.ssl=false","-jar","./kafka-dummy-1.0.jar"]
