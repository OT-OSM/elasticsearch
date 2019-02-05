# osm_elasticSearch_Standalone
This repo controls the Ansible Role for ElasticSearch single node installation.

# Supported OS  

```
Redhat 7
Centos 7
Ubuntu 14/16
Amazon Linux
```

# Dependencies
pyhton  
Java 1.8 or greater 

# Variables/Default for elasticsearch
change below information and uncomment it based on your requirement in var/main.yml file:

```
elasticsearch_version: "6.5.1"
cluster_name: es-cluster

#es_jvm_dump: /var/lib/elasticsearch/heap
#data_path: /var/lib/elasticsearch
#log_path: /var/log/elasticsearch

#elasticsearchIP: "0.0.0.0"
```
# Node defination:
Define your type of nodes in host/inventory file based on below format. 

```
[es]
64.627.16.131 ansible_ssh_user=ubuntu
```
# Example Playbook

```
- hosts: es
  roles:
     - { role: osm_elasticSearch_cluster }
```

# License

BSD

