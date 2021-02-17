# kafka-commando

[Get kafka from here](https://kafka.apache.org/quickstart)
- Have to extract and un tar the kafka version that we downloaded for that we need to git bash it in the C folder where we moved the kafka downloaded file. And the commands for it are as follows.
 ```Bash
$ tar -xzf kafka_2.13-2.7.0.tgz
$ cd kafka_2.13-2.7.0
```
- Now we have to open powershell as admin in the kafka extracted folder and have to run five different commands in five different powershell windows with same path.

```Bash
# Start the ZooKeeper service
# Note: Soon, ZooKeeper will no longer be required by Apache Kafka.
$ bin/zookeeper-server-start.sh config/zookeeper.properties
```
```Bash
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
```Bash
# Start the Kafka broker service
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic bearcat-messages
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```
```Bash
$ bin/kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092
```
```Bash
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
```Bash
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic bearcat-messages --from-beginning
```
