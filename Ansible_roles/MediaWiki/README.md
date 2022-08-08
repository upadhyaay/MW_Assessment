MediaWiki role
==============

This Readme file contains the brief description about the ansible role.
This role is downloading the tar file of mediawiki from the internet and then unarchiving(specific location) it to be used further

Requirements
------------

No prereqs required for this role.

Role Variables
--------------

All variable used in main.yml file are initialized and stated in all.yml inside group.vars (inventory). Please refer for more details.

Example Playbook
----------------

An example of how to use this role (for instance, hardcoding the variable values) is always nice for users too:

    - hosts: servers
      roles:
         - MediaWiki

Details
--------

An optional section for the role authors to include contact information, or a website (HTML is not allowed), if there's any.
