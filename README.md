add-server-to-bareos-backups
=========

Ansible playbook to add a computer to start being backed up by Bareos


How to Use
------------

To use this playbook just run this command.

	1. ansible-galaxy install -r requirements.yml -p roles/ --force
	2. Create a file called .vault_pass in this folder and put a random string in it for decrypting your sensitive variables. Something like: QSkngTv#KTJ=WXpg6qVR
	3. Fill out needed variables in vars/all_vars.yml and vars/vault.yml files
	4. ansible-vault encrypt vars/vault.yml   #Encrypt the sensitive variables

Execution: 
  	
```
	ansible-playbook master.yml -e @vars/all_vars.yml -e @vars/vault.yml -i /Users/Brad/.ansible/hosts
```

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
