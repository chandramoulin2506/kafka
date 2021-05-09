# kafka

The objective is to build an understanding on what is kafka and create a data pipeline to process data using Apache Structured Streaming and Apache Kafka.

![Image](https://github.com/chandramoulin2506/kafka/blob/main/img/kafka_streaming.PNG)


Kafka can be downloaded from https://kafka.apache.org/downloads.
Version used for the below use case 
    • kafka_2.11-0.10.2.2
    • jdk1.8.0_144
    • python 2.7
    • spark-streaming-kafka-0-8-assembly_2.11-2.3.1.jar(downloaded from maven)
    • kafka-clients-0.10.2.2.jar
    • spark-sql-kafka-0-10_2.11-2.3.1.jar
    
untar kafka by below command-

tar -zxvf kafka_2.11-0.10.2.2.tgz -C $HOME
cd kafka_2.11-0.10.2.2

Steps to start the zookeeper and kafka,
Kafka relies on Zookeeper, in order to make it run we will have to run Zookeeper first.

nohup bin/zookeeper-server-start.sh config/zookeeper.properties &
nohup bin/kafka-server-start.sh config/server.properties &

Topic creation:

bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

Listing the topic:
bin/kafka-topics.sh --list --zookeeper localhost:2181
