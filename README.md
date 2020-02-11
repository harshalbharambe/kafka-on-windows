# kafka-on-windows
Running Apache Kafka on Windows

# Running Zookeeper:

zkserver

# Running Kafka:

cd C:\kafka_2.11-2.3.0

.\bin\windows\kafka-server-start.bat .\config\server.properties



# Create Topic named 'test':

.\bin\windows\kafka-topics --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

# Create Producer for 'test':

.\bin\windows\kafka-console-producer --broker-list localhost:9092 --topic test

# Create Consumer for 'test':

.\bin\windows\kafka-console-consumer --bootstrap-server localhost:9092 --topic test --from-beginning


# To delete the topic:

Make entry to server.properties

delete.topic.enable=true

then 

.\bin\kafka-topics.sh --zookeeper localhost:2181 --delete --topic test
