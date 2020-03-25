# ELK on Kubernetes
Deploy Elasticsearch, Logstash, Kibana, Filebeat on Kubernetes

# Getting started
`./run.sh`
or
`kubectl apply -f ${folder-name}`
for the specific module

The order is matter for the dependencies

# Expose
The load-balancer would expose the default port  
```
Elasticsearch:9200
Kibana:5601
```
# Logstash 
`kubectl apply -f ./logstash/`

Copy mysql connector to volume
`kubectl cp --namespace=elk ./logstash/jdbc_driver/mysql-connector-java-5.1.48-bin.jar logstash-0:/usr/share/logstash/jdbc_driver/`