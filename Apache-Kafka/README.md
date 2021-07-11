# Kafka Fundametals

 - ## Distributed Replicated Commit Logs

 - ## Components 
    - ### Broker/Cluster
      - The cluster is nothing but the group of machine connected with each other. Thee broker is nothing but one single machine of cluster. Ideally the broker count should be greater than 2 as this would be used on distributed system. Using only one broker doesn't make any sense in distributed system.

    - ### Zookeeper
      - The Zookeepr is distributed co-ordinated service.

    - ### Producer
      - The Producer in Kafka is an application which sends messages to Kafka broker.

    - ### Consumer
      - The Consumer in Kafka is an application which recieved messages from Kafka broker.

    - ### Message
       - #### Produce
         - The message is being produce by Producer, while producing message there some mandatory fields and some optional fields. The mandatory fields are topic-name, partition-id, and actual message[value] while key is optional. The [key] is used to provide some metadata for message. 

       - #### Storage
         - Once message is recieved by Kafka broker then it get persisted into the brokers partition area. 

       - #### Consume
         - The message is consume by consumer application. 

    - ### Topic
       - #### Logical grouping of message.

    - ### Partition
       - Physical location of message[Stored/Persisted in file system]of a broker.
       - Partition decides degree of parallelism.
       - Ordering of message is it at partition level and which is achieve using offset.
       - There are 3 ways to identify the partition while sending the message to Kafka broker.
          - Mentioned the partition id in message itself.
          - Use key-hash to calculated the partition [hash(key) % partiion_number] -> (0, partition_number-1).
          - Default - Round Robin fashion. 

    - ### Replication
       - Replication is to achieve redudancy and It's default value is 3