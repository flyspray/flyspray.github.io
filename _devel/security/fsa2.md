---
layout: page
title: "Flyspray Security Announcement 2"
---
### Flyspray Cross Site Scripting Vulnerabilities (2007-12-09) 
  
  
<dl class="dl-horizontal">
	<dt>Release Date</dt>
	<dd>2007-12-09</dd>
	<dt>Last Modified</dt>
	<dd>2007-12-09</dd>
	<dt>Author</dt>
	<dd>Cristian Rodriguez <judas.iscariote at flyspray dot org></dd>
	<dt>Application</dt>
	<dd>Flyspray 0.9.9 - 0.9.9.3</dd>
	<dt>Risk</dt>
	<dd>Low</dd>
	<dt>Vendor Status</dt>
	<dd>The Flyspray project has released an updated version</dd>
	<dt>References</dt>
	<dd><http://www.flyspray.org/devel/security/fsa3></dd>
	<dt>Discovered by</dt>
	<dd>KAWASHIMA Takahiro <rivis.kawashima at nifty.com></dd>
<dl>

#### Details

While Flyspray escapes all output variables by default in order to prevent this type of vulnerabilities, some context-dependent problems, caused by the use  of an incorrect escaping strategy has been found.

#### Problem with $\_SERVER['QUERY\_STRING']

Flyspray is affected by a Cross Site scripting Vulnerability due to an error escaping PHP's $_SERVER['QUERY_STRING'] superglobal, that can be maliciously used to inject arbitrary code into the savesearch() javascript function.

#### Problem in the "History" tab 

There is an XSS problem in the history tab, the application fails to sanitize the "details" parameter correctly, leading to the possibility of arbitrary code injection into the getHistory() javascript function.

#### Proof of concept

This vulnerabilies can only be exploited by authenticated users using the following examples

#### QUERY_STRING issue

```
http://example.com/index.php?do=index&dummy=dummy');alert('XSS');void('
```

and then clicking the "OK" button in the "save search as" dialog.

#### "History" tab problem 
 
```
http://example.com/index.php?do=details&task_id=1174&details=');alert('XSS
```
and then clicking in the history tab.


##### Disclosure Timeline

  1. 18, November 2007 - KAWASHIMA Takahiro disclosed vulnerability at security@flyspray.org
  2. 19, November 2007 - possible solution discussed privately
  3. 19, November 2007 - Fix commited the SVN repository
  4. 09, December 2007 - Public disclosure.

##### Recommendation

We strongly recommend to upgrade to the new version.
