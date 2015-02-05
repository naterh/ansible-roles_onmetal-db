onMetal DB disk config
======================

This role configures an onMetal I/O instance for usage as a DB server, includes all the best practice recommendations from Rackspace for getting the most out of the system in terms of performance.

Requirements
------------

/dev/sda and /dev/sdb must be the disk devices, change as required.


Role Variables
--------------

There are only a couple of variables that one may generally want to change.

```yaml
# disk I/O Scheduler: valid values:  cfq | noop | deadline
onmetal_disk_scheduler: noop

# valid values: stripe | mirror (passed to md)
onmetal_disk_mirror_or_stripe: mirror

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
