Ansible script for automating the aws ec2 START and STOP process
=========

There are two roles used for this process. One role is written to stop a cluster of running ec2 instances while the other role is written to start a cluster of stopped ec2 instances.

Requirements
------------
Boto is a Python package that provides interfaces to Amazon Web Services. Boto is the Amazon Web Services (AWS) SDK for Python, which allows developers to write software that makes use of Amazon services. Boto provides an easy to use, object-oriented API as well as low-level direct service access.

So Boto should be installed in the machine running the script.

	- install pip:

		sudo apt-get install python-pip

	- then install boto:

		pip install -U boto


Role Variables
--------------

There are four main variables that need to be updated in this tool.
	Update the access key and the secret key for the aws IAM in the main.yml file inside the defaults folder of each role.
	Include the instance id of the ec2 that needs to be stopped/started in the main.yml of the vars folder. Special care should be taken to preserve the correct order of instance id and it's corresponding ec2 region.



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

To run the script
		$ ansible-playbook stop_aws.yml 

License
-------

BSD

