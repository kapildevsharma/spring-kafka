# Spring Boot Kafka Server 
It's push message from producer and consume message from consumer application in spring boot
In this repo,  find the docker compose file to start entire application and apache kafka server.

First start,
use docker-compose file to start zookeeper and kafka server.
Create Topic with 2 ways
1. 
	docker exec -it broker /bin/bash
	kafka-topics --create --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1 --topic users

	kafka-topics --list --bootstrap-server localhost:9092
2. 
	docker exec broker kafka-topics --create --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1 --topic my-topic
	docker exec broker kafka-topics --list --bootstrap-server localhost:9092
	
	docker exec broker kafka-topics --create --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1 --topic kapil


 After it, run the spring boot application to connect kafka server.
 
Use REST API end point to publish message :
http://localhost:9000/kafka/publish?message=gannu

after it check the log to push and pull message.

	
	
