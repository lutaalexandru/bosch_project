# bosch_project

In this repo you will find:
 - app/ directory which contains the "TODO" application, including the docker-compose.yml file that can be used to build the docker container;
 - the run_app.yml Ansible playbook which can be used to deploy the compleate "Todo" application to a virtual machine defined on hosts file as host1;
 - hosts file (which in fact is /etc/ansible/hosts file - primary inventory for ansible). In this file, under [servers] directive we define the hostname and IP address of the virtual machine on which we want to deploy packages using ansible-playbook.
 
In order to deploy "Todo" application using these files, download them on your Ansible Master machine, setup your inventory (modify the IP address of your controled virtual machine in /etc/ansible/hosts) and run "ansible-playbook run_app.yml" command.

Note: this approach is based on the fact that you already set up your Ansible environment (have made the ssh key exchange between ansible master and ansible controled machines). 
