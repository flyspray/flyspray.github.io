---
layout: manual
title: Install & Setup
manual: start
order: 1
---

## Installing Flyspray 
This document describes the installation process for setting up **Flyspray version 0.9.9.7**. When reading this guide and performing the following install steps, please go in order; Some of the later steps require that the previous steps have been completed, otherwise the installation will fail.



### Preparing for install 
  * Install PHP, MySQL or PostgreSQL, and a web server (like Apache). The latest versions of each should work nicely.
  * For MySQL installations, it's a good idea to install the MySQL Administrator and MySQL Query Browser. Both can be found here: http://dev.mysql.com/downloads/gui-tools/5.0.html
  * In the php.ini file, make sure that the extension php_mysqli.dll is uncommented. The tutorial neglects to include this step.
  * Grab the latest [stable release](/docs/download)
  	 * To use the development version follow [installing from Github](/manual/devel_version)
  * Unpack the compressed package into a directory where your webserver can reach it.
  * Remove the file flyspray.conf.php
  * In the case that the database user you use for your Flyspray installation cannot create a database on its own, create a database for Flyspray to use.
  
```
# mysql -u root -p
  > CREATE DATABASE flyspray DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci; 
  > GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,INDEX,ALTER,CREATE TEMPORARY TABLES ON flyspray.*
          TO flysprayuser@localhost IDENTIFIED BY 'yourpassword'; 
  > quit 
  # mysqladmin -u root -p reload

```

  * Or, create a PostgreSQL database for Flyspray to use:

```
su;
su postgres;
createuser -SDRP flyspray;
createdb -E UNICODE -O flyspray flyspray;
```
  * Make sure the attachments/ and cache/ directory is writeable by the webserver.





### Installation 
  * Point your browser to http://yourserver/flyspray/setup/ and follow along with Flyspray Setup.
  * When Setup completes, you will be automatically logged-in, and taken to your user profile where you can change  details such as your Real Name.
  * A message will tell you to remove the directory http://yourserver/flyspray/setup/

If you would like to enable support for the **local** [Task Dependency Graphs](/manual/dependencies) feature, an additional package must be installed to enable it. Most operating systems have a package available for the free [Graphviz](http://www.graphviz.org/) package, either in an OS-specific package or by download direct from the Graphviz site. After installing Graphviz, add the path to the dot executable to flyspray.conf.php.

### After installation
  * **Enable the reminder daemon** if needed (for reminders, Jabber notifications and background sending of notifications (since 1.0) ), by setting `reminder_daemon = 1` in flyspray.conf.php
  * Click the 'Manage Project' link to set up your project preferences, user groups and lists.
  * Close the sample task, and start adding your own, real tasks.
  * If you need help, read the [manual](/manual), [FAQ](/docs/faq), and [mailing list](/community/mailing-list/) pages.
  * If you want to enable dokuwiki syntax, edit flyspray.conf.php. Change the operand of the **syntax_plugin** statement to `dokuwiki`.
