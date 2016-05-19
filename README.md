# Ansible Roles for setting up some basic applications on Digital Ocean Droplets 

## Disclaimer

I am not a system admin and this is mostly shared so I can discuss and learn. I am currently doing some of the infrastructure for our upcoming Cloud testing service Boozang (http://boozang.com) but will be looking into Docker container deploys and updating the scripts to work with Google Cloud in the near future. The scripts are based very much on Geerlingguy's excellent work on providing helpful scripts in Ansible, and also other people nice enough to share their work publicly. I advise users to go and explore the much more complete references here (https://github.com/geerlingguy). Nevertheless I hope someone might find the examples in here useful. Currently it has only been tested on CentOS 7.0 on DigitalOcean Droplets (https://www.digitalocean.com/), where it works well as the Droplets are very minimally configured and need extra configuration such as enabling SELinux and Fail2Ban, at least for the Wordpress nodes which are extra vulnerable for attacks.


## Requirements
Only tested on CentOS Digital Ocean 7.0 by me. See https://github.com/geerlingguy for complete references and for information on additional platforms. 
Remember to set your server IPs inside the inventory directory to point to your servers. 

## Commands

Deploy on all servers:

ansible-playbook site.yml

Deploy on management servers:

ansible-playbook site.yml -i inventories/management_servers 

Deploy on management servers:

ansible-playbook site.yml -i inventories/database_servers

Deploy on staging servers:

ansible-playbook site.yml -i inventories/staging_servers 

Deploy on production servers:

ansible-playbook site.yml -i inventories/production_servers