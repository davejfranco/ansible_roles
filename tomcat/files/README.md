#Ansible role - tomcat

This role is ment to provide a basic configuration for tomcat7, it requires to install Oracle Java 8 and the role will provide a default tomcat7 settings and tomcat-users.xml



###Example
	---

	- hosts: all
  	  sudo: yes
  	
	  pre_tasks:
 	   - name: update apt cache
 	     apt: update_cache=yes

	  roles:
	   - {role: knopki.locale, locale_all: C, locale_lang: en_US.UTF-8}
	   - {role: ansiblebit.oracle-java, oracle_java_version: 8, oracle_java_set_as_default: True }
	   - {role:tomcat}