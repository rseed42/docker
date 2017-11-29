# Distributed Kafka Setup

## Description

Distributed Kafka setup in its own Docker network.

The system is stateful, because it mounts an external directory (KAFKA_STORE_DIR) where Zookeeper and
Kafka keep their data. This means that data is not lost on restart.

## How to run

1. Create the network "kafka" by issuing "docker network create kafka" if this network is not already present.
2. Edit the KAFKA_STORE_DIR in file ".env" in this directory. This should point to a directory on the computer where docker runs. The directories will be automatically created on startup.
3. Start with "docker-compose up"