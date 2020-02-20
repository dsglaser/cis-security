# cis-security

A role to implement Center for Internet Security (CIS) controls for RHEL (7-8) and RHEL clones (Oracle, CentOS), and Ubuntu 18.04 LTS.

### Introduction

The [Center for Internet Security](https://www.cisecurity.org/) provides a set of
security benchmarks for operating systems designed to decrease the vulnerability vectors of a system.

These benchmarks are published in PDFs for non-commercial use. This role is an implementation of
those controls for Red Hat Enterprise Linux 7 and 8, Oracle Linux 7 and 8, CentOS 7 and 8, and Ubuntu 18.04 LTS. The controls themselves are not published here and
you should visit CIS for a copy of the PDF. These automations are provided as a resposne and a tool to
help systems administrators secure machines based off those recommendations.

This role is designed to layer over other Ansible roles that install packages, users, etc. It should be
idempotent and can be run at any time. As usual with Ansible, make sure that later playbooks don't modify
files that are modified in this role.

Benchmark Versions:
| Operating System | OS Benchmark version |
| -----------------|--------------------- |
| RHEL 7 | v2.2.0 |
| RHEL 8 | v1.0.0 |
| CentOS 7 | v2.2.0 |
| CentOS 8 | v1.0.0 |
| Fedora 31 | (Fedora 28) v1.1.0 |
| Oracle Linux 7 | v2.2.0 |
| Oracle Linux 8 | v1.0.0 |
| Ubuntu 18.04 LTS | v2.0.1 |

### Requirements
To implement the role correctly, you will require the following

- RHEL 7.6+ (or clone) or Ubuntu 18.04 LTS
- Ansible 2.7+
- Machine connected to a package repository source (Satellite or yum repo)

Some of the Ansible modules that are used require Ansible 2.7 and newer.

For most of the role to work, you will need to have a package repo where you can install packages for
a Red Hat machine. Registering with Satellite or a local package repository is recommended before using
this, unless you exclude any tags that install packages.

### Use and Care
The role is designed to run on RHEL 7.6+, RHEL 8+, and Ubuntu 18.04 LTS machines. It may run on associated RHEL and Ubuntu deriviatives, but it has not been tested on them. Upon initiation, the role will automatically detect the OS and run the appropriate task list.

As the role runs, you will see an output listing the control number and a brief description of the
task being performed (or skipped):

```
TASK [security-rollup : 1.7.1.3 - Set SELinux policy to targeted] ******************************
ok: [192.168.122.252]
```

The controls are implemented as Ansible tags. By default all tags are run on a given system. To
disable a tag from running, run the playbook with the tag excluded (--exclude-tags "x.y.z"):

```
ansible-playbook -i <inventory> <playbook.yml> --exclude-tags "x.y.z"
```
Multiple tags can be listed, separated by commas:
```
ansible-playbook -i <inventory> <playbook.yml> --exclude-tags "x.y.z,a.b.c"
```
Note: Some automation tasks handle multiple controls. In the role you may see something like this:

```
- name: 6.1.[2,4] - Ensure permissions on /etc/passwd /etc/group
  file:
    path: /etc/{{item}}
    owner: root
    group: root
    mode: 0644
  loop:
    - passwd
    - group
  tags:
    - 6.1.2
    - 6.1.4
```
* In this control, two tags are being processed, '6.1.2' and '6.1.4' if you want this control to not
run, you must exclude both tags:

```
ansible-playbook -i <inventory> <playbook.yml> --exclude-tags "6.1.2,6.1.4"
```
Some controls are surrouned by Ansible blocks that themselves have tags. Excluding the tag that applies
to the block will exclude all of the tasks inside of the block. If the block's tag is **not** excluded,
then individual tasks inside of the block can be excluded by excluding their tags.

The list of tags and their associated crontol descriptions are listed in the [controls_list](./controls_list.md) file
in this directory.

In addition to tags, there are a number of variables that can be set which will enable or disable
tasks, or set values. These are explained and given default values in the **roles/cis-security/defaults/main.yml**
file. Do not set these values in that file, but create and include your own variable file to override the
defaults or set them as host variables.

### Change Log
- 1/20/2020 - dsglaser@gmail.com - Initial creation
- 1/22/2020 - dsglaser@gmail.com - Added enhanced selinux controls
- 2/18/2020 - dsglaser@gmail.com - Added support for Ubuntu 18.04 LTS, added RHEL clone links