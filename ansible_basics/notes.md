# Installing Ansible

sudo apt update
sudo apt install ansible -y
ansible --version

To get the list of the servers in the hosts file.

ansible all --list-hosts -i <path of inventory file>

ansible all --list-hosts -i ./hosts

ansible webservers --list-hosts -i ./hosts

ansible all -m ping -- To check the connection between various virtual machines

Install sshpass (A utility required for performing ssh using ansible ) -- "sudo apt install sshpass -y"

# Ansible adhoc command

Syntax -- ansible <group> -m <name of the module> -a <parameters>

ansible all -m ping
ansible all -m command -a "hostname"
ansible all -m command -a "df -h"
ansible all -m copy -a "src=./testfile.txt dest=/home/adminuser"
