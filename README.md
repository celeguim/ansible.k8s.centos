# ansible.k8s.centos
# Kubernetes cluster installation using ansible and centos 7

- Prepare 4 virtual machines (2 CPUS and 2G RAM) and adjust the hosts file, i.e.:

[masters]

master ansible_host=192.168.56.101


[workers]

node1 ansible_host=192.168.56.102

node2 ansible_host=192.168.56.103

node3 ansible_host=192.168.56.104


- Copy SSH keys to these servers

- Take the playbook-plan.txt as a guide and voi-lá

ansible-playbook -i hosts centos-initial.yaml -vv

ansible-playbook -i hosts k8s-dependencies.yaml -vv

ansible-playbook -i hosts k8s-master.yaml -vv

ansible-playbook -i hosts k8s-nodes.yaml -vv

ansible-playbook -i hosts k8s-test.yaml -vvv

ansible-playbook -i hosts uninstall.yaml -vv

