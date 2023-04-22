Purpose: Install and deploy a Solr server remotely using Ansible.
Problem it solves: Solr lets users search through NoSQL databases.
Diagram:
	
	Ansible Galaxy Roles	  Ansible Playbook      Ansible.Community.Docker
	-------------------- >>>  ---------------- >>> --------------------------- >>> Solr Server on Container
	  geerlingguy.java	     setup.yml		solr image via eecs proxy 			    
	  geerlingguy.solr			

How to use it:
	1. INSTALL ROLES: ansible-galaxy install -r requirements.yml
	2. INSTALL SOLR ON DEPLOYMENT MACHINE USING ROLES: ansible-playbook setup.yml -K
	3. DEPLOY SOLR IMAGE WITH DOCKER: ansible-playbook docker.yml -K

