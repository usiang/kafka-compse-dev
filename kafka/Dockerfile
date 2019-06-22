FROM java:8

LABEL maintainer="alan <alan@maeteno.com>"

COPY ./kafka_2.12-2.2.0 /kafka

ENV ZOOKEEPER_HOME ${ZOOKEEPER_HOME}

EXPOSE 3306

CMD ["/kafka/bin/kafka-server-start.sh","/kafka/config/server.properties"]