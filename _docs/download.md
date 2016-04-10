---
layout: page
title: "Download"
order: 0
---

## Want to download Flyspray? 

You've come to the right place. Before downloading, you might like to check the [system requirements]({{baseurl}}/docs/requirements). The [manual]({{baseurl}}/manual) might also be helpful for after you download.

### Official Flyspray Downloads

<table class="table">
<thead>
	<tr>
		<th>Release Type</th>
		<th>Download</th>
		<th>Notes</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td rowspan="2">1.0 RC1 release</td>
		<td>As .zip:<br/>
		<a href="https://github.com/Flyspray/flyspray/archive/v1.0-rc1.zip">https://github.com/Flyspray/flyspray/archive/v1.0-rc1.zip</a><br/>As .tar.gz:<br/>
		<a href="https://github.com/Flyspray/flyspray/archive/v1.0-rc1.tar.gz">https://github.com/Flyspray/flyspray/archive/v1.0-rc.tar.gz</a>
		</td>
		<td>Current recommended stable release</td>
	</tr>
	<tr>
		<td>Precompiled with 3rd party libs for PHP5.2 and PHP5.3: 
		<a href="http://flyspray.org/packed/flyspray-1.0-rc1_php53.tgz">flyspray-1.0-rc1_php53.tgz</a>
		<br/><br/>Precompiled with 3rd party libs for PHP5.4: 
		<a href="http://flyspray.org/packed/flyspray-1.0-rc1_php54.zip">flyspray-1.0-rc1_php54.zip</a>
		<br/>
		<a href="http://flyspray.org/packed/flyspray-1.0-rc1_php54.tgz">flyspray-1.0-rc1_php54.tgz</a>
		<br/><br/>Precompiled with 3rd party libs for PHP5.5:
		<a href="http://flyspray.org/packed/flyspray-1.0-rc1_php55.zip">flyspray-1.0-rc1_php55.zip</a>
		<br/>
		<a href="http://flyspray.org/packed/flyspray-1.0-rc1_php55.tgz">flyspray-1.0-rc1_php55.tgz</a>
		<br/><br/>Precompiled with 3rd party libs for PHP5.6:
		<a href="http://flyspray.org/packed/flyspray-1.0-rc1_php56.tgz">flyspray-1.0-rc1_php56.tgz</a>
		</td>
		<td>For people who cannot run composer on command line on their web hosting: releases that contain all required 3rd party libraries in one .zip or .tgz for different versions of PHP</td>
	</tr>
	<tr>
		<td rowspan="2">1.0 RC release</td>
		<td>As .zip: <a href="https://github.com/Flyspray/flyspray/archive/v1.0-rc.zip">https://github.com/Flyspray/flyspray/archive/v1.0-rc.zip</a><br/>As .tar.gz: <a href="https://github.com/Flyspray/flyspray/archive/v1.0-rc.tar.gz">https://github.com/Flyspray/flyspray/archive/v1.0-rc.tar.gz</a>
		</td>
		<td>First "release candit" release</td>
	</tr>
	<tr>
		<td>Precompiled with 3rd party libs for PHP5.2 and PHP5.3: <a href="http://flyspray.org/packed/flyspray-1.0-rc_php533.tgz">flyspray-1.0-rc_php533.tgz</a>
		</td>
		<td>For people who cannot run composer on command line on their web hosting: releases that contain all required 3rd party libraries in one .zip or .tgz for different versions of PHP</td>
	</tr>
	<tr>
		<td>Development</td>
		<td><a href="https://github.com/flyspray/flyspray">Flyspray @ Github</a></td>
		<td> See <a href="/manual/devel_version">Installing from Github</a> - not recommended for production</td>
	</tr>
</tbody>
</table>

#### Updating from previous versions 

  * Create a backup of your files and database
  * Remove **all files** except the /attachments/ , /avatars/ (since FS1.0 alpha), /vendors/ directories and /flyspray.conf.php
   * Copy the new files to the Flyspray directory
  * make sure flyspray.conf.php is writeable by the webserver.
  * Run the upgrader at http://yourflyspray/setup/ (detects upgrade needed and guides you)
  * Remove the /setup folder after all went fine.


#### Alpha and Beta releases

Alpha releases may still contain critical bugs and are subject to changes without notice. Alpha packages can be updated without version changes.

* We recommend these releases to advanced users
* Downloading these versions will get you the newest features available.
* Beta versions contain every features that the final product will have.
* We await from alpha and beta users that they report us bugs they encounter using our bug tracker: [file bugs](http://bugs.flyspray.org)


#### Development Release

Make sure you know what you are getting into before you download the bleeding edge version of Flyspray!

* Downloading this version will get you the newest features and you will have access to stuff the exact second the developers start releasing them.
* However, this also means you may encounter bugs and other unintended side effects. Make sure to [file bugs](http://bugs.flyspray.org) and follow the [Flyspray mailing list]({{baseurl}}/community/mailing-list)
 

### Past Releases
 *  **[Flyspray 1.0 Alpha 2](http://flyspray.org/packed/flyspray-1.0.alpha2.zip)** - 04 April 2015
 *  **[Flyspray 1.0 Alpha](http://flyspray.org/packed/flyspray-1.0.alpha.zip)** - 16 March 2015
 *  **[Flyspray 0.9.9.7](http://flyspray.org/packed/flyspray-0.9.9.7.zip)** - 28 May 2012, <strong>SHA1SUM:</strong> 056C192BD0FB07905E537869E55D4298D384D6C9
 *  **Flyspray 0.9.9.6** - 01 May 2009
 *  **Flyspray 0.9.9.5.1** - 24 March 2008
 *  **Flyspray 0.9.9.5** - 24 February 2008
 *  **Flyspray 0.9.9.4** - 12 December 2007
 *  **Flyspray 0.9.9.3** - 23 August 2007

### Donate
Although using Flyspray is free, developing it does cost money. [Please consider donating a few dollars via Paypal to help fund development](https://www.paypal.com/xclick/business=connect@thevelozgroup.com&amp;item_name=Flyspray+Donation&amp;no_shipping=1&amp;no_note=1&amp;tax=0).
