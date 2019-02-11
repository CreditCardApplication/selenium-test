# Cloudera hadoop 5.14.4 installation using ansible
These Ansible playbooks will help to deploy hadoop cluster for Cloudera on any number of nodes. 
We support most commonly used linux flavors like: CentOS 7, RedHat 7 and it’s prerequisites on the listed OS. 

# Requirements
* Ansible >= 2.1.
* Expects RHEL/CentOS 7

# Features
* The biggest advantage is that user just need to define Hadoop distribution as a variable. User doesn’t need to know specifics of Cloudera,  or  deployment information. 
* Single hosts file for all Hadoop distribution.
* It installs Cloudera using cloudera API v19
* No upper limit on number of nodes.
* Single command will deploy entire cluster once couple of files are updated with hosts and other info.
* Playbooks allows user to select custom repositories. This helps to select local repositories is any which saves considerable amount of network bandwidth and time.
* One can fine tune parameter which are supported by blueprints for Cloudera API for Cloudera.
* Easy to add custom deployment scripts to existing playbooks if you need to install additional software.
* One can easily tweak Simple Ansible playbooks if they have some specific requirement.
* Can be used for on premise or cloud deployments.

# Configuration
* For running playbook,you need to configure hosts, group_vars/all, and group_vars/passwords.yml files only.
* For more details about hosts and group_vars files see [hosts.md]and [all_vars.md]


# Installation
* To install Hadoop: **ansible-playbook -i hosts site.yml -u `<USER>` -k --ask-vault-pass**  
Password for vault is: **vault**

# Accessing Ambari / Cloudera Management Console  
Once Cloudera manager is installed, hadoop components installation can be monitored as mentioned below:
* for Cloudera GUI: go to `<Master-ip>`:7180  
**credentials: admin/admin**  

# License  
Apache Licence v2

# Author Information
Vinod Patil, Shailesh Vaidya
- vinod.patil5@wipro.com
- shailesh.vaidya@wipro.com
