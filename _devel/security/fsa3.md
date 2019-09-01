---
layout: page
title: "Flyspray Security Announcement 3"
---

### Flyspray Cross Site Scripting Vulnerabilities (2008-02-11) 
<dl class="dl-horizontal">
	<dt>Release Date</dt>
	<dd>2008-02-24</dd>
	<dt>Last Modified</dt>
	<dd>2008-02-24</dd>
	<dt>Author</dt>
	<dd>Florian Schmitz <floele at flyspray dot org></dd>
	<dt>Application</dt>
	<dd>Flyspray 0.9.9 - 0.9.9.4</dd>
	<dt>Risk</dt>
	<dd>Low</dd>
	<dt>Vendor Status</dt>
	<dd>The Flyspray project has released an updated version</dd>
	<dt>References</dt>
	<dd><http://www.flyspray.org/devel/security/fsa3></dd>
	<dt>Discovered by</dt>
	<dd>Digital Security Research Group (DSecRG)</dd>
<dl>


#### Details 


While Flyspray escapes all output variables by default in order to prevent this type of vulnerabilities, some more hidden problems have been found.

#### Problem with SQL errors 

Flyspray is affected by a Cross Site scripting Vulnerability due missing escaping of SQL error messages. By including HTML code in a query and at the same time causing it to fail by submitting invalid data, an XSS hole can be exploited.

#### Problem in the task history attached to comments 

There is an XSS problem in the task history attached to comments, since the application fails to sanitize the the *old_value* and *new_value* database fields for changed task summaries.


##### Proof of concept

The Flyspray team will not release an example exploit to the public.

##### Disclosure Timeline

  1. 08 February 2008 - DSecRG disclosed vulnerability at security@flyspray.org
  2. 11 February 2008 - Fix committed the SVN repository
  3. 24 February 2008 - Public disclosure.

##### Recommendation

We strongly recommend to upgrade to the new version.
