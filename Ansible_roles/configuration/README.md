configuration role
==============

This Readme file contains the brief description about the ansible role. This role contains the Post install configurations for apache server and further configurations for firewall and selinux services.

Requirements
------------

Apache is to be preinstalled before running this role.

Role Variables
--------------

All variable used in main.yml file are initialized and stated in all.yml inside group.vars (inventory). Please refer for more details.

Example Playbook
----------------

An example of how to use this role (for instance, hardcoding the variable values) is always nice for users too:

    - hosts: servers
      roles:
         - configuration

Details
--------

An optional section for the role authors to include contact information, or a website (HTML is not allowed), if there's any.