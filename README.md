[![Build Status](https://travis-ci.org/wahidsadik/ansible-role-apache.svg?branch=master)](https://travis-ci.org/wahidsadik/ansible-role-apache)

TBD
===

- Galaxy
- Testing it out
- Update readme
  - Identify dependencies
  - Examples
  - Requirements
+ Create GH repo
+ Travis integration

Role Name
=========

An Ansible role to install Apache with basic hardening.

The role is available on Ansible Galaxy: [https://galaxy.ansible.com/wahidsadik/ansible-apache-role](https://galaxy.ansible.com/wahidsadik/ansible-role-apache).

To add this role from Ansible Galaxy, run: `ansible-galaxy install wahidsadik.ansible-role-apache`.

To add this from your Ansible `requirements.yml`, add this to the file:

    src: wahidsadik.ansible-role-apache


Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

The role defines the following variables in `defaults/main.yml`:

    www_root: /var/www
    www_user: deployer
    www_group: www-data

>Notes:
>
> - `www_user` **must belong** to `www_group` group.
> - `www_user` **should not be** `root` user for security reasons.


Users must pass the following parameters (i.e. variables):

- None

Dependencies
------------

The role depends on the following roles:

- TBD
- TBD

The `remote_user` used run this role should be able change permission of directories and files usually owned by `root`. Hence, you will probably need to `sudo` to successfully run use this role. See examples for more details.

Example Playbook
----------------

Show examples of:

- With simplest possible variables
- With non-root user and in simplest possible variables
- With non-root user with full (and if needed other combinations) variable sets

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: wahidsadik.ansible-role-apache, x: 42 }

License
-------

MIT

Author Information
------------------

Wahid Sadik

Repo: [https://github.com/wahidsadik/ansible-role-apache](https://github.com/wahidsadik/ansible-role-apache).
