# Docker environments

This repo contains popular OpenSource infrastructure components:

Component      | Compose file                         | Comments
-------------- | ------------------------------------ | ----------------------------
elasticsearch  | elasticsearch/compose.yml            | ElasticSearch
elasticsearch  | elasticsearch/compose-opendistro.yml | OpenDistro for ElasticSearch
kibana         | kibana/compose.yml                   | Kibana
kibana         | kibana/compose-opendistro.yml        | OpenDistro for ElasticSearch (Kibana)
prometheus     | prometheus/compose.yml               | Prometheus
grafana        | grafana/compose.yml                  | Grafana
zipkin         | zipkin/compose.yml                   | Zipkin
jaeger         | jaeger/compose.yml                   | Jaeger
keycloak       | keycloak/compose.yml                 | KeyCloak (single instance)
keycloak       | keycloak/compose-cluster.yml         | KeyCloak (standalone cluster)
postgresql     | postgresql/compose.yml               | PostgreSQL
oracle-xe      | oracle-xe/compose.yml                | Oracle Database XE 
redis          | redis/compose.yml                    | Redis
mongo          | mongo/compose.yml                    | MongoDB
openldap       | openldap/compose.yml                 | OpenLDAP
sftp-server    | sftp-server/compose.yml              | sFTP server
kafka          | kafka/compose.yml                    | Kafka distribution with Kafka Connect UI, Kafka Topics UI, Confluent Schema Registry and REST Proxy
kafka          | kafka/compose-cp.yml                 | Confluent Platform OSS distribution (Kafka & Zookeeper)
schema-registry | schema-registry/compose.yml         | Confluent Schema Registry
kafka-rest-proxy | kafka-rest-proxy/compose-cp.yml    | Confluent REST proxy
rabbitmq       | rabbitmq/compose.yml                 | RabbitMQ
wso2am         | wso2am/compose.yml                   | WSO2 API Manager
activemq       | activemq/compose.yml                 | Apache ActiveMQ Classic
activemq-artemis | activemq-artemis/compose.yml       | Apache ActiveMQ Artemis
swagger-ui     | swagger-ui/compose.yml               | Swagger UI
apicurio-registry | apicurio-registry/compose.yml     | Apicurio Registry
otel-collector | otel-collector/compose.yml           | OpenTelemetry Collector
kong           | kong/compose.yml                     | Kong Gateway
## Running

All the following docker-compose commands should be run from this directory.

You may want to remove any old containers to start clean:
```
docker rm kafka zookeeper keycloak prometheus grafana kibana elasticsearch jaeger postgresql
```
### Popular bundles
##### ElasticSearch & Kibana
You can startup all the containers at once:
```
docker-compose -f compose.yml -f elasticsearch/compose.yml -f kibana/compose.yml up --remove-orphans
```
Or, you can have multiple terminal windows and start individual component in each:
```
docker-compose -f compose.yml -f elasticsearch/compose.yml up

docker-compose -f compose.yml -f kibana/compose.yml up
```
##### Prometheus & Grafana
You can startup all the containers at once:
```
docker-compose -f compose.yml -f prometheus/compose.yml -f grafana/compose.yml up --remove-orphans
```
Or, you can have multiple terminal windows and start individual component in each:
```
docker-compose -f compose.yml -f prometheus/compose.yml up

docker-compose -f compose.yml -f grafana/compose.yml up
```
