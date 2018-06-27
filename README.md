Apigee OPDK Setup Ansible Controller Backup
=========

This role will backup an Ansible controller that was setup using the role [Apigee OPDK Setup Ansible Controller](https://github.com/carlosfrias/apigee-opdk-setup-ansible-controller). 

Requirements
------------

* This roles will read attributes stored in the Ansible cache by the [Apigee OPDK Setup Ansible Controller](https://github.com/carlosfrias/apigee-opdk-setup-ansible-controller)
* This script will backup the settings of Ansible Control server. 

Role Variables
--------------

A description of the variables for this role can be found below: 

| Variable | Description |
| --- | --- |
| target_download_folder | This is the path where backups should be kept |
| target_download_pattern | This collection is the list of files that should be retrieved and stored as a backup. This collection follows the convention: `- { dir: "{{ inventory_folder }}/", pattern: '*' }` | 

Dependencies
------------

This role depends on the Ansible role [Apigee OPDK Setup Ansible Controller](https://github.com/carlosfrias/apigee-opdk-setup-ansible-controller) to store values in the Ansible cache. 

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: {{ target_hosts }}
      roles:
         - apigee-opdk-setup-ansible-controller-backup
         
    ansible_playbook      

License
-------

Apache 2.0

Author Information
------------------

Carlos Frias
