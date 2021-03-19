# Hadoop Multinode Cluster Using Ansible  

<img src="https://juststickers.in/wp-content/uploads/2014/07/Hadoop.jpg" height=100 width=170 alt="Kubernetes" /> <img src="https://gorillalogic.com/wp-content/uploads/2016/10/maxresdefault-1.jpg" height=100 width=170 alt="Ansible" /> <img src="https://www.metaltoad.com/sites/default/files/styles/large_personal_photo_870x500_/public/2020-05/aws-logo-blog-header.png?itok=t4o3meiH" height=100 width=170 alt="AWS" />

This repository contains the Ansible Playbook and Roles to deploy Hadoop Multi-node cluster over AWS EC2 Instances.  
  
### Ansible Roles -   

**Role Name** | **Role Description**
------------- | --------------------
**awsInfra4Hadoop** | To create a AWS Infrastructure for Hadoop MultiNode Cluster
**HadoopNameNode** | To configure Hadoop Name Node  
**HadoopDataNode** | To configure Hadoop Data Node

## Prerequisites   
- Ansible should be installed and Configured
- AWS CLI Should be Installed and Configured  
- Other requirements of Roles are included in Readme file of particular Role

## How to Start 
- Clone or Download the Repository  
- Change the value of variables according to requirement  
- Finally run setupHadoopCluster.yml using 'ansible-playbook setupHadoopCluster.yml' command  

## Note  
- Recommended to use RedHat AMI or OS for Hadoop Name and Data Nodes  
- Ansible Config file should include previliage_escalation block to become root user in order to configure AWS Instances  

# Links

[Click here for Video and Post](https://www.linkedin.com/in/amanjhagrolia143)
  
***Feel free to Contact if any issue!!***

<a href="https://www.linkedin.com/posts/amanjhagrolia143_vimaldaga-righteducation-educationredefine-activity-6778537176985587712-XVGt" target="_blank"> <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /> </a> 
<a href="https://galaxy.ansible.com/jhagdu" target="_blank"> <img src="https://galaxy.ansible.com/assets/galaxy-logo-02.svg" height=30 width=140 /> </a>
