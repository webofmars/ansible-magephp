Ansible Role: magephp
========================

Build status for this role: [![Build Status](https://travis-ci.org/webofmars/ansible-magephp.svg?branch=master)](https://travis-ci.org/webofmars/ansible-magephp.svg?branch=master)


This role installs and configures magallanes / magephp on a linux system with PHP > 5.3 running on it.

Requirements
------------

PHP-cli > 5.3

Role Variables
--------------

Available variables are listed below, along with default values :

```
magephp_version: "1.2.1"
magephp_archive_filename: "v{{ magephp_version }}.tar.gz"
mage_php_archive_url: "https://github.com/magephp/magallanes/archive/{{ magephp_archive_filename }}"
magephp_dl_dir: "/tmp"
magephp_extract_dir: "/tmp/ansible-magephp"
magephp_icmd_dir: "{{ magephp_extract_dir }}/magallanes-{{ magephp_version }}"
magephp_install_dir: "/opt/magephp"
magephp_install_cmd: "bin/mage install --systemWide --installDir={{ magephp_install_dir }}"
magephp_verify_path: "/usr/bin/mage"
```

Dependencies
------------

None.

Example Playbook
----------------
```
- hosts: all
  become: yes
  become_method: sudo
  roles:
    - role: webofmars.magephp
```
This example will install magephp.


License
-------

GPLv3


Author Information
------------------

Created by Frederic Leger / webofmars.