Role Name
=========

This role uses the scadalts-linux-installer in order to install mysql, java and tomcat and serve a Scada-LTS instance.

Requirements
------------

This role was tested on Ubuntu 24.04 and on Ubuntu 22.04. So, we can only guarantee its working on these operating systems.

Role Variables
--------------

scadalts_basepath - defines where to save the whole mysql, java and tomcat stuff
scadalts_ubuntu2204 - defines, whether Ubuntu 22.04 is used (by default, this value is set to false, because we assume Ubuntu 24.04 as default-OS)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Install and configure ScadaLTS
  hosts: hmi
  roles:
    - role: acr-ansible-scadalts
      become: true
      vars:
        scadalts_basepath: /opt/scadalts
        scadalts_ubuntu2204: false
