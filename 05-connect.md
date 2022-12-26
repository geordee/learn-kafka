# Kafka Connect

Kafka Connect is a free, open-source component of Apache Kafka® that works as a centralized data hub for simple data integration between databases, key-value stores, search indexes, and file systems.

## Install

```bash
mkdir /usr/local/kafka/plugins
vi /usr/local/kafka/config/connect-distributed.properties
# see root/usr/local/kafka/config/connect-distributed.properties
```

## Create Topics

```bash
mkdir /usr/local/kafka/scripts
vi /usr/local/kafka/scripts/create_local_topics
# see root/usr/local/kafka/scripts/create_local_topics
chmod +x /usr/local/kafka/scripts/create_local_topics
/usr/local/kafka/scripts/create_local_topics
```

## Start

```bash
$KAFKA_HOME/bin/connect-distributed.sh $KAFKA_HOME/config/connect-distributed.properties
curl http://localhost:8083/connectors
```

## Elasticsearch Plugin

```bash
confluent-hub install confluentinc/kafka-connect-elasticsearch:latest \
   --component-dir /usr/local/kafka/plugins \
   --worker-configs /usr/local/kafka/config/connect-distributed.properties

curl -d @/usr/local/kafka/config/connect-elasticsearch-sink.json -H "Content-Type: application/json" -X POST http://localhost:8083/connectors
curl http://localhost:8083/connectors
```

## Test

```bash
$KAFKA_HOME/bin/kafka-console-producer.sh --topic hello-elasticsearch --broker-list localhost:9092
>{ "subject": "hello world", "body": "Hello World is a small piece of code to illustrate a language's basic syntax." }
```
