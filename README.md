# ansible
Playing about with ansible configuration.

# Basic how to run it locally:
ansible all -i 'localhost,' -c local -m ping
#-i localhost, runs it locally instead of on an inventory. 
#-c local, connects locally instead of trying to ssh to a remote server.
#-m specifies a module 'ping' in this case.

#we could make a inventory file that contains:
#localhost ansible_connection=local
#This would allow us to run the same as above with:
ansible all -i /tmp/my-inventory -m ping

#expected inventory seems to be /etc/ansible/hosts
ansible localhost -m ping

#to run:
ansible-playbook playbook.yml

#To Do
Mumble



