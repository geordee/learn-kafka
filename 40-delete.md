# Delete Records

```bash
$KAFKA_HOME/bin/kafka-delete-records.sh --bootstrap-server localhost:9092 --offset-json-file /tmp/offsets.json
```

In the file, the offset specified should bes one higher than the problematic offset reported in the listener log. For example, specifying an offset of 3 means the command deletes all messages from the beginning up to offset 3.
