Lab - Notification by external commands
=======================================

* Inspect the default e-mail notification in `/etc/icinga2/conf.d/commands.conf`
* Copy the config to a directory that will be loaded in Icinga 2

```
cp -a /etc/icinga2/conf.d/commands.conf /etc/icinga2/local.d/commands-mail.conf
```

* Reload icinga2
* Re-Run Director Kickstart

* Create user template `mail-user`
* Create user `linuxadmin` using template `mail-user`

* Create notification templates `mail-host-notification` and `mail-service-notification`
* Create notification apply `linux host`
    - Using template `mail-host-notification`
    - Selecting user `linuxadmin`
    - assign where `host.templates contains "linux host"`
* Create similar notification apply `linux service`
