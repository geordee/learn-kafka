# Kafka Topics

## Topics

Create
```bash
$KAFKA_HOME/bin/kafka-topics.sh --create --topic hello-elasticsearch --bootstrap-server localhost:9092
```

Describe
```bash
$KAFKA_HOME/bin/kafka-topics.sh --describe --topic tars-events --bootstrap-server localhost:9092
```

List
```bash
$KAFKA_HOME/bin/kafka-topics.sh --list --bootstrap-server localhost:9092
```

Delete
```bash
$KAFKA_HOME/bin/kafka-topics.sh --delete --topic hello-elasticsearch --bootstrap-server localhost:9092
```
