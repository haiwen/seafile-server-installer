Important: The repository is maintained at [Seafile/seafile-server-installer](https://github.com/Seafile/seafile-server-installer) now.

# Auto install Seafile Server CE* and PRO**

These installers offer a quick and easy way to set up a production ready Seafile Server using MariaDB, Memcached and NGINX as a reverse proxy in under 5 minutes.

\* Community Edition
** Professional Edition

## What's it for?
Install the [Seafile Server](http://seafile.com/en/home/) in a standard and more secure manner then our current out of the box setup scripts offer. Instead of SQLite we're using MariaDB and NGINX instead of Gunicorn.


## Why?
There are too many ways to misconfigure a manual Seafile server installation. We've noticed that many people don't realize that the default installation is very unsafe. In other cases people get stuck during the manual installation procedure or forget a step like changing `FILE_SERVER_ROOT` or use IP addresses instead of resolvable DNS names.


Visit the main project at https://github.com/SeafileDE/seafile-server-installer for further details.
