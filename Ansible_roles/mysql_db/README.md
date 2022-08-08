mysql_db role
=========

This Readme file contains the brief description about the ansible role.
In this role some configurations are to be done on installed database.

Requirements
------------

SQL is to be installed into the VM which is done in the Xampp role. Consider running that before this.

Role Variables
--------------

All variable used in main.yml file are initialized and stated in all.yml inside group.vars (inventory). Please refer for more details.

Example Playbook
----------------

An example of how to use this role (for instance, hardcoding the variable values) is always nice for users too:

    - hosts: servers
      roles:
         - mysql_db

Details
--------

An optional section for the role authors to include contact information, or a website (HTML is not allowed), if there's any.
