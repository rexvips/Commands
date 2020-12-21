# Kafka Command line 

**Kafka Consumer**  
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic _TOPIC_NAME_ --from-beginning   
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic _TOPIC_NAME_  
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic _TOPIC_NAME_ --offset 10 --partition 0  

**Kafka Producer**   
./kafka-console-producer.sh --broker-list localhost:9092 --topic _TOPIC_NAME_  

**Get Offset**  
./kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic _TOPIC_NAME_ --time -1  

**List all topics**  
./kafka-topics.sh --list --zookeeper localhost:2181  

**Create topic in Kafka**  
./kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 2 --topic _TOPIC_NAME_  
./kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic _TOPIC_NAME_  

**DELETE A TOPIC in KAFKA**  
./kafka-topics.sh --zookeeper localhost:2181 --delete --topic _TOPIC_NAME_  
  
**GET Count of number of messsages in KAFKA TOPIC**  
./kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic _TOPIC_NAME_

**List the topics to which the group is subscribed**  
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --group _CONSUMER_GROUP_NAME_ --describe

