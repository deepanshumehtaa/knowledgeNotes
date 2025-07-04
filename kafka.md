### Apache Kafka is a distributed event streaming platform used for real-time data processing, where producers send messages (events) to Kafka topics and consumers read those messages
with several core components that work together to provide its functionality. 


## Here's a breakdown of its main components:

> Core Components:
1. Producer	==> Applications that publish (write) events to Kafka topics
2. Consumer	==> Applications that subscribe to (read and process) events from topics
3. Broker	==> A Kafka server that stores data and serves client requests
4. Topic	==> A category/stream name to which records are published (like a database table)
5. Partition	==> Topics are split into partitions for parallelism and scalability
6. Offset	==> A unique ID assigned to each message within a partition (like a primary key)
7. Consumer Group	A group of consumers that jointly consume a topic (each message goes to only one consumer in the group)

Workflow diagram:

![image](https://github.com/user-attachments/assets/e6141d1a-fb36-4493-b240-3674fa1db795)

Task Scheduling:

![image](https://github.com/user-attachments/assets/954132bd-936c-4d7f-9ed6-2fd7e05d88e2)



## How about kafka as Task Queues ??
```
              | Kafka                          | RabbitMQ 
Data Model	  | Persistent log (append-only)	| Ephemeral queues (FIFO)
Task ACKs	    | Manual offset commits         | Built-in ACK/NACK
Retries	      | No native retry logic         | retry mechanisms
Priority	    | No native support	            | Priority queues available
```

## connecting to kafka has many ways (protocol):
1. PLAINTEXT
2. SSL (Secure Sockets Layer) i.e. SSL/TLS encrypts data in transit between clients and brokers.
3. SASL_SSL (Simple Authentication and Security Layer)
   mechanisms:
     PLAIN (username/password)
     GSSAPI (Kerberos)
     SCRAM (Salted Challenge Response Authentication Mechanism)
5. SASL_PLAINTEXT

Q: what is Kerberos ?
A: Is SSO auth protocol, Three Main Components:
1. Client: The user or service requesting access to a resource.
2. Server: The resource or service being protected.
3. Key Distribution Center (KDC): A trusted 3rd party system that manages authentication.


