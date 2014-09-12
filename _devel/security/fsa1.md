---
layout: page
title: "Flyspray Security Announcement 1"
---
### Flyspray Administrator authentication bypass (2007-03-16) 

|               |            |
|---------------|------------|
| Release Date  | 2007-03-16 |
| Last Modified | 2007-04-04 (added CVE references) |
| Author        | Cristian Rodriguez <judas.iscariote at flyspray dot org> |
| Application   | Flyspray 0.9.9 |
| Risk          | High |
| Vendor Status | The Flyspray project has released an updated version |
| References    | http://www.flyspray.org/fsa:1, [CVE-2007-1788](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2007-1788)|
| Discovered by | Stefan Esser <sesser at hardened-php dot net> |

#### Details
Flyspray authentication system can be bypassed by sending a carefully crafted post request.
To be vulnerable, PHP configuration directive output_buffering has to be disabled or set to a low value.   


#### Proof of concept
The Flyspray team will not release an example exploit to the public.

#### Disclosure Timeline

  1. 13, March 2007 - vulnerability discovered by Stefan Esser
  2. 13, March 2007 - possible solution discussed privately
  3. 13, March 2007 - Fix commited the SVN repository
  4. 16, March 2007 - Public disclosure.

#### Recommendation
We strongly recommend to upgrade to the new version.
