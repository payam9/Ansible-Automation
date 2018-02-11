# Ansible-Automation

first you need to install ansible
 pip install ansible

 you can create a vagrant machine like this:

 Vagrant init bento/centos-7.3

 vagrant up

 Vagrant ssh           //to start the machine

 vagrant reload        // if any changes

 Logout

 Vagrant destroy       //to destroy the machine

then you can use the play book to automate the tasks:

ansible webserver -m ping -i ansible/hosts.ini          // ping the vagrant machin and AWS

ansible webserver --list-hosts -i ansible/hosts.ini      // give you the hosts

ansible-playbook ansible/playbook.yml -i ansible/hosts.ini   //run the playbook

you need to change the IP Address in the hosts.

also you need to get your own private key and change it in the host in order to connect to AWS SSH

at this point we only need to add some line to playbook to deploy the HTMl file.
