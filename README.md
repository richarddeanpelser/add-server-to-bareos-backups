add-server-to-bareos-backups
=========

Ansible playbook to add a computer to start being backed up by Bareos


How to Use
------------

To use this playbook just run this command.

	1. ansible-galaxy install -r requirements.yml -p roles/ 
	2. ansible-playbook master.yml -e @vars/all_vars.yml -i /Users/Brad/.ansible/hosts

Requirements
------------

You need to have an already setup and working version of Bareos (version 17+)

Variables
------------

See the `vars/all_vars.yml` file for a full list


Roles
------------

	- stancel.install-bareos-client
	- stancel.setup-mysql-backups
	- stancel.add-job-to-bareos-director
