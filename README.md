# Auto install Seafile Server CE* and PRO**

These installers offer a quick and easy way to set up a production ready Seafile Server using MariaDB, Memcached and NGINX as a reverse proxy in under 5 minutes.

\* Community Edition
** Professional Edition

## What's it for?

Install the [Seafile Server](http://seafile.com/en/home/) in a standard and more secure manner then our current out of the box setup scripts offer.


## Supported OS

Just select the corresponding installer for your OS. All scripts are meant to run with the bare minimum OS setup. We strongly suggest not installing Seafile server besides desktop environment or hosting panels like Plesk, ISPConfig, etc. Professional installations which don't follow our setup suggestions, don't qualify for official support. Keep this in mind.

### Minimal installations only!

1. Ubuntu 16.04/18.04
2. CentOS 7/8

## Caution
Never run these scripts on a production server. They are more or less a one trick pony and could seriously damage production systems. Run it only once and
delete it afterwards. If something goes wrong, restart with a fresh machine.

As a precaution I have added a few simple checks to abort installation if any of these fails:

1. Check if you're running this script as root. If not, abort.
2. Check if the user "seafile" exists. If yes, abort.
3. Check if the directory "/opt/seafile" exists. If yes, abort.


## Feature overview
1. HTTP-Proxy
2. Seahub with WSGI
3. [Seafile WebDAV (aka. SeafDAV)](https://download.seafile.com/published/seafile-manual/extension/webdav.md) with FastCGI
4. MariaDB
5. Memcached
6. Seafile auto start
7. Firewall


## Installation

For Seafile Professional Server, you will have to download the package prior to the installation and save it to /opt/.

- For Seafile 7.1.x

    For **CentOS 8 (64bit)**
    ```bash
    cd /root
    wget --no-check-certificate https://raw.githubusercontent.com/haiwen/seafile-server-installer/master/seafile-7.1_centos
    bash seafile-7.1_centos **7.1.x**
    ```
    
    For **Ubuntu 18.04/20.04 (64bit)**
    ```bash
    cd /root
    wget --no-check-certificate https://raw.githubusercontent.com/haiwen/seafile-server-installer/master/seafile-7.1_ubuntu
    bash seafile-7.1_ubuntu **7.1.x**
    ```
    where instead of "7.1.x" specify proper sub-version

- For Seafile 6.x.x/7.0.x

    For **CentOS 7 (64bit)**
    ```bash
    cd /root
    wget --no-check-certificate https://raw.githubusercontent.com/haiwen/seafile-server-installer/master/seafile_centos
    bash seafile_centos 7.0.5
    ```
    
    For **Ubuntu 16.04/18.04 (64bit)**
    ```bash
    cd /root
    wget --no-check-certificate https://raw.githubusercontent.com/haiwen/seafile-server-installer/master/seafile_ubuntu
    bash seafile_ubuntu 7.0.5
    ```


## FAQs

***What's the unprivileged Seafile users name?***
seafile

***How can I login as the unprivileged Seafile user?***
Run `su - seafile -s /bin/bash` with root privileges on the shell

***How do I update Seafile?***
You will have to handle Seafile updates/upgrades manually after the initial installation. Consult http://manual.seafile.com/deploy/upgrade.html on how to upgrade Seafile.

To login as the Seafile users run `su - seafile -s /bin/bash` and then proceed with the update procedure as usual.

BTW: Ideas on how to automate upgrades are very welcome!

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
