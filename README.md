# bosch_project

In this repo you will find:
 - app/ directory which contains the "TODO" application, including the docker-compose.yml file that can be used to build the docker container;
 - the run_app.yml Ansible playbook which can be used to deploy the compleate "Todo" application to a virtual machine defined on hosts file as host1;
 - hosts file (which in fact is /etc/ansible/hosts file - primary inventory for ansible). In this file, under [servers] directive we define the hostname and IP address of the virtual machine on which we want to deploy packages using ansible-playbook.
 - video of running the paybook in order to deploy "Todo" application on one virtual machine;
 
In order to deploy "Todo" application using these files, download them on your Ansible Master machine and setup your inventory (modify the IP address of your controled virtual machine in /etc/ansible/hosts). You will also need an "ansible_user" user defined on both machines and the ssh key exchange done between those two hosts (if you want to use a different user for this setup please change the all appearances of ansible_user with your local user account on the run_app.yml file.
After finishig with this setup, on your master machine, as user "ansible_user" (or your local user) run "ansible-playbook run_app.yml" command (from directory where you download the application).
