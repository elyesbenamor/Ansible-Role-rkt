
# Ansible Role: rkt
hetha update remotly
=======
hetha change loocally
[![CI](https://github.com/geerlingguy/ansible-role-kubernetes/workflows/CI/badge.svg?event=push)](https://github.com/geerlingguy/ansible-role-kubernetes/actions?query=workflow%3ACI)

An Ansible Role that installs [Rkt](https://coreos.com/rkt/docs/latest/) on Linux.

Rkt Install
=========

Usage for install and start the Rkt container runtime in linux.

Role Variables
--------------

| Variable's name | Description | Example |
| --------------- | ----------- | ------- |
| rkt.debian_version  | version of Rkt that you want install. Default's 1.8.0  | 1.8.0  |
|rkt.rpm| version of rpm is 1.29|rkt-1.29.0-1.x86_64.rpm|
|image_path|http://www.example.com/cool-thing.aci|he path to the ACI |
|service_name|rkt-run |the name of the service|


Example 
----------------

Install from Galaxy:

	$ ansible-galaxy install elyesbenamor.ansible_role_rkt

Playbook (for default variables):

    - hosts: all
      roles: 
      	- elyesbenamor.ansible_role_rkt

Playbook (for specific variables):

    - hosts: all
      roles:
      	- { role: elyesbenamor.ansible_role_rkt, rkt_version: 1.9.0 }


Then, log into the master, and run `rkt version` as ubuntu non root user, and you should see the version of your runtime rkt.

## Useful links

Use try [rkt with kubernetes](https://coreos.com/rkt/docs/latest/using-rkt-with-kubernetes.html) to see how to integrate the rkt runtime on your cluster.

License
-------

MIT

Author
------

ELyess ben amor
