# Event Streaming

## Producer

```bash
$KAFKA_HOME/bin/kafka-console-producer.sh --topic topic-name --broker-list localhost:9092
```

```bash
$KAFKA_HOME/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic topic-name --property "parse.key=true" --property "key.separator=|"
```

## Consumer

```bash
$KAFKA_HOME/bin/kafka-console-consumer.sh --topic topic-name --from-beginning --bootstrap-server localhost:9092
```
