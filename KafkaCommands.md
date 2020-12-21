# Kafka Command line 

**Kafka Consumer**  
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic TOPIC_NAME --from-beginning   
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic TOPIC_NAME  
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic TOPIC_NAME --offset 10 --partition 0  

**Kafka Producer**   
./kafka-console-producer.sh --broker-list localhost:9092 --topic TOPIC_NAME  

**Get Offset**  
./kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic TOPIC_NAME --time -1  

**List all topics**  
./kafka-topics.sh --list --zookeeper localhost:2181  

**Create topic in Kafka**  
./kafka-topics.sh --create --bootstrap-server qaKafka:9092 --replication-factor 1 --partitions 2 --topic TOPIC_NAME  
./kafka-topics.sh --create --zookeeper qaKafka:2181 --replication-factor 1 --partitions 1 --topic TOPIC_NAME  

**DELETE A TOPIC in KAFKA**  
./kafka-topics.sh --zookeeper kafka:2181 --delete --topic TOPIC_NAME  
  
**GET Count of number of messsages in KAFKA TOPIC**  
./kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic TOPIC_NAME
