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

## How to import/export kibana saved objects

Under management, navigate to saved objects. Clicking the links takes to you to a page listing containing all saved items.

On the top right corner there is an export/import feature.


To create a backup click the export button and provide the file path where the items should be stored then complete your import action.

To import your backup file, click the import button and upload the json file. Complete these action by clicking done!