#Ansible role - mongodb

This role provide a vanilla installation of mongodb, it has capabilities to install differents
version of mongo.

###Variables
	version: "version to install" type= float
###Default values

	version: 3.0.6
###Example
	---
	- hosts: vagrant
  	  sudo: true


	  roles:
	   - {role: knopki.locale, locale_all: C, locale_lang: en_US.UTF-8}
	   - {role: mongodb}


