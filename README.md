[![Build Status](https://travis-ci.org/wahidsadik/ansible-role-apache.svg?branch=master)](https://travis-ci.org/wahidsadik/ansible-role-apache)

Role Name
=========

An Ansible role to install Apache with basic hardening.

The role is available on Ansible Galaxy: [https://galaxy.ansible.com/wahidsadik/ansible-apache-role](https://galaxy.ansible.com/wahidsadik/ansible-role-apache).

To add this role from Ansible Galaxy, run: `ansible-galaxy install wahidsadik.ansible-role-apache`.

To add this from your Ansible `requirements.yml`, add this to the file:

    src: wahidsadik.ansible-role-apache


Requirements
------------

None

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

The `remote_user` used run this role should be able change permission of directories and files usually owned by `root`. Hence, you will probably need to `sudo` to successfully run use this role. See examples for more details.

Example Playbook
----------------

Example 1: Simplest example with minimum variable passing

    - hosts: servers
      remote_user: root
      roles:
         - { role: wahidsadik.ansible-role-apache}

Example 2: With sudo and minimum variable passing

    - hosts: servers
      remote_user: deployer
      become: true
      become_method: sudo
      roles:
      - { role: wahidsadik.ansible-role-apache }

Example 3: Overriding additional variables

    - hosts: servers
      remote_user: deployer
      become: true
      become_method: sudo
      roles:
      - { role: wahidsadik.ansible-role-apache, www_root: /var/web, www_user: myuser, www_group: www}

License
-------

MIT

Author Information
------------------

Wahid Sadik

Repo: [https://github.com/wahidsadik/ansible-role-apache](https://github.com/wahidsadik/ansible-role-apache).
