Role Name
=========

# common setup centos7

```
* disable selinux
* disable firewalld
* setup sysstat
* stop noise rsyslogd

* set timezone, locale
  localectl set-timezone
  localectl set-locale

* package install:
      - "rsync"
      - "git"
      - "bind-utils"
      - "sysstat"
      - "dstat"
      - "wget"
      - "openssl"
      - "nkf"
      - "net-tools"
      - "yum-utils"

* history setting
  /etc/profile.d/history.sh
```

Requirements
------------
None

Role Variables
--------------

```
locale: ja_JP.UTF-8
zone: Asia/Tokyo
```


Dependencies
------------
None

Example Playbook
----------------

    - hosts: servers
      vars:
        zone: UTC
      roles:
         - common

