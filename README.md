Owncloud - A docker based installation
=========

This role installs owncloud and postgres docker images, and sets up cron to do periodic database dumps (currently only on Sundays at 3am).

Once installed, to connect to the database use host "owncloud-database" username "owncloud" and password "owncloud".

Requirements
------------

This role requires docker to be installed on the host.

Role Variables
--------------

```
owncloud_apps_dir: /opt/owncloud/apps
owncloud_config_dir: /opt/owncloud/config
owncloud_data_dir: /opt/owncloud/data
owncloud_database_dir: /opt/owncloud/database-files
owncloud_database_backups_dir: /opt/owncloud/database-backups
```

Dependencies
------------

Docker must be installed on the host.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: lndobryden.owncloud,
              owncloud_apps_dir: /opt/owncloud/apps,
              owncloud_config_dir: /opt/owncloud/config,
              owncloud_data_dir: /opt/owncloud/data,
              owncloud_database_dir: /opt/owncloud/database-files,
              owncloud_database_backups_dir: /opt/owncloud/database-backups }

License
-------

BSD

Author Information
------------------

Lee Dobryden - https://github.com/lndobryden
