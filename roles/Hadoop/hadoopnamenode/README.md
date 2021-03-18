HadoopNameNode
==============

Ansible Role to configure Hadoop Name Node

Requirements
------------

Recommended target systems are RHEL or Centos

Role Variables
--------------

    # Port No. of Hadoop Name Node to be used
    hadoop_name_port: "9000"

Dependencies
------------

Recommended to use with jhagdu.hadoopdatanode Role which configures Hadoop Data Node

Example Playbook
----------------

    - hosts: servers
      vars:
        - hadoop_name_port: "9000"
      roles:
         - jhagdu.hadoopnamenode

License
-------

BSD

Author Information
------------------

Author Name: Aman Jhagrolia  
Contact: https://www.linkedin.com/in/amanjhagrolia143  
