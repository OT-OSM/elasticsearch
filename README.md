Ansible Role: osm_elasticsearch
=========
An ansible role to install and configure elasticsearch standalone setup.

Version History
---------------

|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|**June '15** | v.1.0 | Initial Draft | Sudipt Sharma |

Supported OS
------------
  * Redhat : 7
  * CentOS : 7
  * Ubuntu : 14/16
  * Amazon Linux

Dependencies
------------
* Java 1.8 or higher
* python

# Variables/Default for elasticsearch
change below information and uncomment it based on your requirement in var/main.yml file:

```
elasticsearch_version: "6.5.1"
cluster_name: es-stanalone

#es_jvm_dump: /var/lib/elasticsearch/heap
#data_path: /var/lib/elasticsearch
#log_path: /var/log/elasticsearch

#esIP: "0.0.0.0"
```
Inventory
----------
An inventory for elasticsearch setup should look like this:-
```ini
[elastichost]                 
192.168.1.198    ansible_user=ubuntu   
192.168.3.201    ansible_user=opstree 
```
Example Playbook
----------------

* Here is an example playbook:-

```
- hosts: es
  roles:
     - { role: osm_elasticSearch }
```
* ansible-playbook elastic.yml

# License

BSD

