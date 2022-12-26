# Install Kafka

## Install

```bash
sudo apt install default-jre
sudo apt install openjdk-8-jre-headless

cd temp/
wget https://downloads.apache.org/kafka/3.3.1/kafka_2.13-3.3.1.tgz
tar -xvzf kafka_2.13-3.3.1.tgz
sudo mv kafka_2.13-3.3.1 /usr/local/kafka
```

## Start

With Zookeeper

```bash
$KAFKA_HOME/bin/zookeeper-server-start.sh $KAFKA_HOME/config/zookeeper.properties
$KAFKA_HOME/bin/kafka-server-start.sh $KAFKA_HOME/config/server.properties
```

With Kraft

```bash
KAFKA_CLUSTER_ID="$($KAFKA_HOME/bin/kafka-storage.sh random-uuid)"
# KAFKA_CLUSTER_ID=LSBoqJhRR4aFkGVNl8ACtQ
$KAFKA_HOME/bin/kafka-storage.sh format -t $KAFKA_CLUSTER_ID -c $KAFKA_HOME/config/kraft/server.properties
$KAFKA_HOME/bin/kafka-server-start.sh $KAFKA_HOME/config/kraft/server.properties
```
