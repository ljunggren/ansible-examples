# Ansible Roles for setting up some basic infrastructure in Ansible. 

## Disclaimer

I am not a system admin and this is mostly shared so I can discuss and learn as I am currently doing some of the infrastructure for our upcoming Cloud testing service Boozang (Http://boozang.com). It's based very much on Geerlingguy's excellent work on providing helpful scripts in Ansible. I advise users to go to the source and explore the more complete references here (https://github.com/geerlingguy).  Nevertheless I hope someone might find the examples in here useful.Currently it has only been tested on CentOS 7.0 on DigitalOcean Droplets (https://www.digitalocean.com/), where it works well as the Droplets are barebone and need extra configuration such as enabling SELinux and Fail2Ban, at least for the Wordpress nodes which are extra vulnerable for attacks.


## Requirements
Only tested on CentOS Digital Ocean 7.0 by me. See https://github.com/geerlingguy for complete references and for information on additional platforms. 
Remember to set your server IPs inside the inventory directory to point to your server. 

## Commands
ansible-playbook site.yml -i inventories/management_servers 
ansible-playbook site.yml -i inventories/database_servers 
ansible-playbook site.yml -i inventories/staging_servers 
ansible-playbook site.yml -i inventories/production_servers