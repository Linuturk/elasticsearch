#ElasticSearch
This Ansible role will install and setup elasticsearch on all hosts specified and place them in the same cluster.

##Supported Distros
Build to support any class of RedHat or Debian based distros, only tested on CentOS 6.5 and Ubuntu 12.04

##Default Configuration
By default all hosts specified will:
* Have a random node name.
* Be eligible for master election.
* Use unicast discovery as multicast is unreliable in cloud environments.

##Usage
See examples directory for example playbook files

##Recommendations
It is recommended to use this playbook with at least 3 servers so that the cluster can be quorate.

##Contributions
Please make sure to review the style guidelines and conform to them.  Please make sure that you fully understand the
layout we are using before making hierarchical changes.

##License
This rolebook is licensed under the Apache License v2.0, see LICENSE.md.
