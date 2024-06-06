# Auto install Seafile Server

> Note, installation script will no longer be maintained for Seafile v12 and later versions. Please use Docker based installation method instead.


These installers offer a quick and easy way to set up a production ready Seafile Server using MariaDB, Memcached and NGINX as a reverse proxy in under 5 minutes.

Ubuntu 20.04/22.04 are supported now.


## Caution

Do not run these scripts on a production server that you have already a Seafile running. 

As a precaution, a few simple checks to abort installation if any of these fails:

1. Check if you're running this script as root. If not, abort.
2. Check if the user "seafile" exists. If yes, abort.
3. Check if the directory "/opt/seafile" exists. If yes, abort.


## Feature overview

1. HTTP-Proxy
2. Seahub with WSGI
3. [Seafile WebDAV (aka. SeafDAV)](https://download.seafile.com/published/seafile-manual/extension/webdav.md) with  WSGI
4. MariaDB
5. Memcached
6. Seafile auto start
7. Firewall


## Installation

For Seafile Professional Server, you will have to download the package prior to the installation and save it to /opt/.

For Seafile 8.0.x or newer versions on **Ubuntu 18.04/20.04 (64bit)** server

```bash
cd /root
wget --no-check-certificate https://raw.githubusercontent.com/haiwen/seafile-server-installer/master/seafile-8.0_ubuntu
bash seafile-8.0_ubuntu 8.0.0
```

Replace the version number to the version number you use if you're using newer versions.


## FAQs

***What's the unprivileged Seafile users name?***

seafile

***How can I login as the unprivileged Seafile user?***

Run `su - seafile -s /bin/bash` with root privileges on the shell

***How do I update Seafile?***

You will have to handle Seafile updates/upgrades manually after the initial installation. Consult http://manual.seafile.com/deploy/upgrade.html on how to upgrade Seafile.

To login as the Seafile users run `su - seafile -s /bin/bash` and then proceed with the update procedure as usual.

***What do I have to do after the installer has finished?***

1. Delete installer script. You wont need it anymore and might even seriously damage your system if you run it again.
2. Follow the suggested steps at the end of the installation to finalize your Seafile server installation.


## License

Copyright (c) 2016, Seafile Ltd.

Copyright 2015, Alexander Jackson

This program is free software: you can redistribute it and/or modify
it under the terms of the [GNU Affero General Public License](http://www.gnu.org/licenses/agpl-3.0.html) as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.
