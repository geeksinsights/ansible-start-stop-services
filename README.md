# ansible-start-stop-services

This play book is to start and stop all services at once for services like for respective environment only
- Postgres & Pgpool
- Kafka/Zookeeper
- ELK
- Cassandra
- Redis/Sentinel/Stunnel
- Prometheus


Pre-requisities
- Hosts file
  You must keep the hosts in groups and call the group in ansible run command line
  ex:-
  [env-services]
  where env is prd/stg/qa/dev anything
  where service is specific to above Postgres, Pgpool, Elasticsearch, Kibana, Cassandra, Redis, Sentinel, Stunnel, Prometheus
  
Running Playbook
- Clone the playbook

- Modify Hosts files according to your need

- Run playbook for entire dev hosts for all services Pgpool, postgres, cassandra, prometheus, cassandra, redis, sentinel, stunnel, kafka, zookeeper etc
  Ex: ansible-play-book stop.yml -i hosts --extra-vars "env=dev"
  
- Run playbook for dev but only one technology
  Ex: ansible-play-book start.yml -i hosts --extra-vars "env=dev, tech=cassandra"
  

