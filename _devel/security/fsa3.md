---
layout: page
title: "Flyspray Security Announcement 3"
---

### Flyspray Cross Site Scripting Vulnerabilities (2008-02-11) 

|               |            |
|---------------|------------|
| Release Date  | 2008-02-24 |
| Last Modified | 2008-02-24 |
| Author        | Florian Schmitz <floele at flyspray dot org> |
| Application   | Flyspray 0.9.9 - 0.9.9.4 |
| Risk          | Low |
| Vendor Status | The Flyspray project has released an updated version |
| References    | http://www.flyspray.org/fsa:3|
| Discovered by | Digital Security Research Group (DSecRG) |


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
  2. 11 February 2008 - Fix commited the SVN repository
  3. 24 February 2008 - Public disclosure.

##### Recommendation

We strongly recommend to upgrade to the new version.
