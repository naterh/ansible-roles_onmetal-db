onMetal DB disk config
======================

This role configures an onMetal I/O instance for usage as a DB server, includes all the best practice recommendations from Rackspace for getting the most out of the system in terms of performance.

Requirements
------------

/dev/sda and /dev/sdb must be the disk devices, change as required.


Role Variables
--------------

There is really only one variable that one may generally want to change:

```yaml
onmetal_disk_scheduler: noop
```

Example Playbook
----------------

Sample play:

```yaml
---

- hosts: disk
roles:
- { role: ansible-roles_onmetal-db-disk-config }
```

License
-------

BSD
