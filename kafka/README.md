# Kafka Fundametals

 - ## Components 
    - ### Broker/Cluster
      - The cluster is nothing but the group of machine connected with each other. Thee broker is nothing but one single machine of cluster. Ideally the broker count should be greater than 2 as this would be used on distributed system. Using only one broker doesn't make any sense in distributed system.

    - ### Zookeeper
      - The Zookeepr is distributed co-ordinated service.

    - ### Producer

    - ### Consumer

    - ### Message
       - #### Produce
         - The message is being produce by Producer, while producing message there some mandatory fields and some optional fields. The mandatory fields are topic-name, partition-id, and actual message[value] while key is optional. The [key] is used to provide some metadata for message. 
       - #### Storage

       - #### Consume

    - ### Topic

    - ### Partition

    - ### Replication
       - Replication is to achieve redudancy and It's default value is 3