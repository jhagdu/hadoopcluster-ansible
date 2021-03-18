HadoopDataNode
==============

Ansible Role to configure Hadoop Data Node

Requirements
------------

Recommended target systems are RHEL or Centos

Role Variables
--------------

    # Pass IP of Hadoop Name Node here
    # Data nodes will be joined with this Name node
    # Examples :- 
    #     hadoop_name_ip: localhost
    #     hadoop_name_ip: 192.143.66.7
    #     hadoop_name_ip: "{{ groups.HadoopNameNode }}"
    hadoop_name_ip: "127.0.0.1"


    # Port No. of Hadoop Name Node
    hadoop_name_port: "9000"

Dependencies
------------

Recommended to use with jhagdu.hadoopnamenode Role which configures Hadoop Name Node

Example Playbook
----------------

    - hosts: servers
      vars:
        - hadoop_name_ip: "127.0.0.1"
        - hadoop_name_port: "9000"
      roles:
         - jhagdu.hadoopdatanode

License
-------

BSD

Author Information
------------------

Author Name: Aman Jhagrolia  
Contact: https://www.linkedin.com/in/amanjhagrolia143  
