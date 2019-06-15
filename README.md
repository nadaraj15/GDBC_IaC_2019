# GDBC_IaC_2019
GDBC Event  2019 

Steps to Execute Ansible commands

How to Install Ansible in linux vm

https://docs.microsoft.com/en-us/azure/virtual-machines/linux/ansible-install-configure#install-ansible-on-an-azure-linux-virtual-machine

Setup credentials (Service Principle)

https://docs.microsoft.com/en-us/azure/virtual-machines/linux/ansible-install-configure#create-azure-credentials

Check and verify ansible version

ansible --version

Add host IP
/etc/ansible/hosts

TO make ansible to ask for password instead of ssh
export ANSIBLE_HOST_KEY_CHECKING=False

Check connectivity

ansible <hostname> -m ping --ask-pass -u naddyuser

ansible -m shell -a 'free -m' apache  --ask-pass -u naddyuser

To execute Ansible Playbook

ansible-playbook <file_name.yml>


ansible-playbook <file_name.yml> -vvvvv  --ask-pass -u naddyuser

or

ansible-playbook <file_name.yml> -vvvvv --ask-pass -u naddyuser  -bK 


Deploy Azure VM

sudo ansible-playbook AzureVM.yml

Install Tomcat

sudo ansible-playbook tomcat.yml  --ask-pass -u <username>

Install MySQL

sudo ansible-playbook mysql.yml  --ask-pass -u <username>
