# ansible.k8s.centos
Kubernetes cluster installation using ansible and centos 7

Prepare 4 virtual machines (2 CPUS and 2G RAM) and adjust the hosts file, i.e.:

[masters]
master ansible_host=192.168.56.101

[workers]
node1 ansible_host=192.168.56.102
node2 ansible_host=192.168.56.103
node3 ansible_host=192.168.56.104

