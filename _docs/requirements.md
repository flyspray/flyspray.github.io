---
layout: page
title: "System Requirements"
---

This information is valid only for Flyspray **1.0** or later

### Overview 

  * A computer to act as a server.
  * Web server software. We use Apache for testing, so this is the official supported. For nginx or others, look at htaccess.dist file and adapt the config for you web server.
  * The [PHP](http://php.net) version minimal 5.3.2, PHP 5.4 or later recommended.
  * PHP-GD library.
  * [MySQL]([http://www.mysql.com) or [PostgreSQL](http://www.postgresql.org) server. MYSQL 5.x and later and Postgresql 8.x or later are tested, older versions may or may not work, you are encouraged to report success or failures to the mailing list.
  * The XML extension is *required* for Jabber (OpenSSL *recommended*) and *required* for setup and upgrades.
  * A working [SMTP server](http://www.postfix.org)  to be used as a replacement of the PHP mail() function  is *highly recommended* but not required.
