# Docker environments

This repo contains popular OpenSource infrastructure components

Component      | Compose file                         | Comments
-------------- | ------------------------------------ | ----------------------------
elasticsearch  | elasticsearch/compose.yml            | ElasticSearch
elasticsearch  | elasticsearch/compose-opendistro.yml | OpenDistro for ElasticSearch
kibana         | kibana/compose.yml                   | Kibana
kibana         | kibana/compose-opendistro.yml        | OpenDistro for ElasticSearch
prometheus     | prometheus/compose.yml               |
grafana        | grafana/compose.yml                  |
zipkin         | zipkin/compose.yml                   |
jaeger         | jaeger/compose.yml                   |
keycloak       | keycloak/compose.yml                 | Single instance
keycloak       | keycloak/compose-cluster.yml         | Standalone cluster
postgresql     | postgresql/compose.yml               | 
redis          | redis/compose.yml                    | 
mongo          | mongo/compose.yml                    | 
openldap       | openldap/compose.yml                 | 
sftp-server    | sftp-server/compose.yml              | 
kafka          | kafka/compose.yml                    | Kafka distribution with Apache Kafka, Kafka Connect, Zookeeper, Confluent Schema Registry and REST Proxy (includoing kafka-topics-ui, schema-registry-ui, kafka-connect-ui)
kafka          | kafka/compose-cp.yml                 | Confluent distribution
rabbitmq       | rabbitmq/compose.yml                 |
wso2am         | wso2am/compose.yml                   | WSO2 API Manager   
swagger-ui     | swagger-ui/compose.yml               |
