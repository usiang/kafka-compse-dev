FROM java:8

LABEL maintainer="alan <alan@maeteno.com>"

COPY ./kafka_2.12-2.2.0 /kafka

ARG BROBER_ID
ARG ZOOKEEPER_HOST

RUN sed -i 's/BROBER_ID/'${BROBER_ID}'/g' /kafka/config/server.properties && \
sed -i 's/ZOOKEEPER_HOST/'${ZOOKEEPER_HOST}'/g' /kafka/config/server.properties

EXPOSE 9092

CMD ["/kafka/bin/kafka-server-start.sh","/kafka/config/server.properties"]