AWSInfra4Hadoop
===============

Ansible Role to create a AWS Infrastructure for Hadoop MultiNode Cluster

Requirements
------------

AWSCLIv2 should be installed and configured  
  
Required Python Packages -  
- boto  
- boto3  
- botocore  
- python >= 2.6  

Role Variables
--------------

Variables which should be included in additional variable files -  

    # Specify AWS CLI Profile to be Used
    aws_profile: default


    #### Ansible Paths ####
    # Path to ansible config directory
    ans_conf_dir: /etc/ansible/
    # Path to ansible inventory file
    ansible_inv_path: /etc/ansible/hosts/hosts.txt


    #### AWS Subnets ####
    ## These two subnets should have connectivity between then
    # For Hadoop Name Node
    nn_subnet_id: "subnet-85efd5ed"
    # For Hadoop Data Nodes
    dn_subnet_id: "subnet-85efd5ed"


    #### AMI IDs ####
    ## Recommended To use RedHat Linux
    # For Hadoop Name Node
    nn_ami_id: "ami-0a9d27a9f4f5c0efc"
    # For Hadoop Data Nodes
    dn_ami_id: "ami-0a9d27a9f4f5c0efc"


    #### Specify Instance Types ####
    # For Hadoop Name Node
    nn_inst_type: "t2.micro"
    # For Hadoop Data Nodes
    dn_inst_type: "t2.micro"


    #### Your Public CIDR ####
    # This Public CIDR/IP is allowed through Security Group of Name Node
    # So that Name Node can be accessible to Clients
    #
    # If not specified, then by default 0.0.0.0/0 will be allowed
    # That is Name Node is vulnerable as it is publically open
    pub_cidr: "0.0.0.0/0"


    # Port Number for Hadoop Name Node Server
    name_node_port: 9091

    # Number of Data Nodes for Hadoop cluster
    no_of_data_nodes: 2


Variables in defaults/main.yml -  

    # Default Hadoop Ports

    ## Name Node WebUI
    # Over HTTP
    name_webui_http: 50070
    # Over HTTPS
    name_webui_https: 50470

    ## Name Node Metadata Services
    name_meta_svc1: 8020
    name_meta_svc2: 9000

    ## Data Node WebUI
    # Over HTTP
    data_webui_http: 50075
    # Over HTTPS
    data_webui_https: 50475

    # Data Node Data Transfer Port
    data_transfer_port: 50010

Variables in vars/main.yml -  

    # Key-pair name for Kubernetes Nodes
    hadoop_key_name: hadoopkey

    #### Security Groups Name ####
    # For Master Node
    nn_sg_name: namesg
    # For Worker Nodes
    dn_sg_name: datasg

Dependencies
------------

No Dependencies on other roles or collections

Example Playbook
----------------

aws_hadoop_infra.yml is a additional variable file that contains required variables -

    - hosts: servers
      vars_files:
         - aws_hadoop_infra.yml
      roles:
         - jhagdu.awsinfra4hadoop

License
-------

BSD

Author Information
------------------

Author Name: Aman Jhagrolia  
Contact: https://www.linkedin.com/in/amanjhagrolia143  
