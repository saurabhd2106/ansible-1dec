# Installing Ansible

sudo apt update
sudo apt install ansible -y
ansible --version

To get the list of the servers in the hosts file.

ansible all --list-hosts -i <path of inventory file>

ansible all --list-hosts -i ./hosts

ansible webservers --list-hosts -i ./hosts