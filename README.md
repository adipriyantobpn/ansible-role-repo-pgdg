Ansible Role: PostgreSQL PGDG Repository
=========

An Ansible Role that to manage PostgreSQL PGDG Yum repository

Requirements
------------

This role needs no special requirements, except sudo access

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):


```yaml
---
repo_location:              international   # available options: international, vagrant
pgdg_enabled:               yes
pgdg_version:               9.4
```

Dependencies
------------

None

Example Playbook
----------------

We can use this roles multiple times with different `pgdg_version` like this:

```yaml
---
- name: Prepare CentOS 7 server
  hosts: centos7
  roles:
    - role: adipriyantobpn.repo-pgdg
      repo_location:              vagrant
      pgdg_enabled:               yes
      pgdg_version:               9.4
    - role: adipriyantobpn.repo-pgdg
      repo_location:              international
      pgdg_enabled:               no
      pgdg_version:               9.5
    - role: adipriyantobpn.repo-pgdg
      repo_location:              international
      pgdg_enabled:               no
      pgdg_version:               9.6
```

License
-------

BSD

Author Information
------------------

This role was created in 2017 by [Adi Priyanto](https://github.com/adipriyantobpn) as a learning purpose for community.