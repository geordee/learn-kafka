# Kouncil

Kouncil provides an easy-to-use Apache Kafka web GUI for performing various operations such as observing consumer and broker groups, monitoring cluster health, debugging processes, or browsing and reviewing topics in a clear layout.

## Start

```bash
podman run -d --network=host -e bootstrapServers="localhost:9092" consdata/kouncil:latest
```
