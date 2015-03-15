---
layout: page
title: "Security"
order: 300
---

This document describes how security incidents are handled since Flyspray **0.9.9**.

### Reporting and handling security problems. 

  * Write a detailed report to <security@flyspray.org> and we will contact you privately.

  * We take security so damn seriously, that we **promise** to release an update in **no more than 5 business days** if the problem reported:
   - Is **remotely** exploitable, such as XSS(and friends), remote code execution or SQL Injection.
   - It discloses **critically sensitive** user information (passwords, the **contents** of other files in the system..).
   - All other type of issues considered 'minor' will be fixed in the next patch level release in conjunction with other bugs. 
  * We will write an FSA (Flyspray Security Announcement) describing the vulnerability briefly **after** the release of a minor, patch level release. the FSA may contain source code patch against the previous release.
  * We will thank you for your report and give proper credits. 




### Flyspray 0.9.9 

  * 2008-02-24 [Cross site scripting (XSS) vulnerabilities](/devel/security/fsa3)
  * 2007-12-14 [Cross site scripting (XSS) vulnerabilities](/devel/security/fsa2)
  * 2007-03-16 [Admin authentication bypass](/devel/security/fsa1)
  

### Security problems archive 

You can read a list of known security problems on [Flsypray's Secunia.com page](http://secunia.com/product/5995/?task=advisories)




### Things that are NOT security holes in Flyspray

PHP security holes, where the only real solution is to upgrade your PHP version to be protected.

Also, There are a few third party flyspray integrations that we are aware of :

  * Mambo/Joomla Flyspray
  * active-factory
  * A modified version included with EGroupware.

Please **do not** contact us about vulnerabilities in that products, **unless** the problem is present in **officially supported** Flyspray releases available in either the download section or in the **active branches** of our Git repository. 

We have no control of the code included in that tools.  
