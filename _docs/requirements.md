---
layout: page
title: "System Requirements"
---

This information is valid only for Flyspray **1.0** or later

### Overview 

  * A computer to act as a server.
  * Web server software. We use Apache for testing, so this is the official supported. For nginx or others, look at htaccess.dist file and adapt the config for you web server.
  * [PHP](http://php.net) 5.4 up to current PHP 7.3
  * PHP-GD library
  * [MySQL]([http://www.mysql.com) or [PostgreSQL](http://www.postgresql.org) server. MySQL 5.x (MySQL >5.5 recommended) and later and Postgresql 8.x or later are tested, older versions may or may not work, you are encouraged to report success or failures to bugs.flyspray.org or the mailing list.
  * The XML extension is *required* for Jabber (OpenSSL *recommended*) and *required* for setup and upgrades.
  * A working [SMTP server](http://www.postfix.org) to be used as a replacement of the PHP mail() function  is *highly recommended* but not required.
