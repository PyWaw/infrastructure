# PyWaw Infrastructure

This repository contains provisioning and deployment scripts for all
[PyWaw](http://pywaw.org) sites and services.
 
## Requirements

Following command will install all requirements:

    $ pip install -r requirements.txt
    
We suggest you to run it in Python 2.x virtualenv.
        
## Usage

We are using [Ansible](http://http://www.ansible.com) tool to manage our 
server(s) and deploy all sites and services. Each project has separate 
directory, e.g. main PyWaw site scripts are located in `pywaw.org/` directory.
You could find there playbooks, vars, templates and other artefacts.

If you want to run playbook, you have to pass also inventory file as 
argument. In example below, we are deploying production version of `pywaw.org`
site:

    $ ansible-playbook pywaw.org/playbooks/deploy.yml -i hosts.ini -e settings=production