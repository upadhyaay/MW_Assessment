service role
=========

This Readme file contains the brief description about the ansible role.
In this role just restarting some services.

Requirements
------------

Maria DB and httpd services are up and running.

Role Variables
--------------

All variable used in main.yml file are initialized and stated in all.yml inside group.vars (inventory). Please refer for more details.

Example Playbook
----------------

An example of how to use this role (for instance, hardcoding the variable values) is always nice for users too:

    - hosts: servers
      roles:
         - service

Details
--------

An optional section for the role authors to include contact information, or a website (HTML is not allowed), if there's any.
