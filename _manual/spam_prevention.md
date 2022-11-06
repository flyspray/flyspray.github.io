---
layout: manual
title: Spam Prevention
manual: admin
author: peterdd
order: 31
---

## Prevention

* When having only a fixed amount of users (e.g. company internal users), disable user registering at **Admin Toolbox->Preferences->User Registration** and add new users manually in the **Admin Toolbox->Users and Groups->Register New User**

* Even if some spammers today found ways to circumvent CAPTCHAs, you can enable CAPTCHAs at **Admin Toolbox->Preferences->Spam Prevention**

* Use confirmation codes for new registrations. This requires the spammer to use a valid email address to register. This makes it a bit more expensive for spammers as it takes more time to offload their mess and require them to have/buy an automated throwaway-emailaccounts-confirmation loop.

* Alternatively use 'Registrations approved by admins' option in **Admin Toolbox->Preferences->User Registration**

Often spammer use generated email accounts that follow certain pattern and even when you don't know your users you get a feeling what registration could be a spam account. But you can't be 100% sure as they often use mass mail providers like gmail, so also real people often have not so nice address names that can look similiar to to typical spammer email addresses.

* Limit the load a user can do. I thought of limiting the number of comments and tasks a user can create per day or having a user credit/trust/rating system. But all that has also their disadvantages and I have not yet started implementing.

* Use external spam reducing tools that block/suspend/slowing down suspicious IPs/email addresses or behavior. Think of fail2ban or even third party lists (whitelisting, greylisting, blacklisting)


## How to handle if it happened?

I can only tell how I handle it where I am a Flyspray admin:

### Spam Account

If I clearly know it is just a spam account and not a misused/hacked normal user account:

1. Disable the spam user account and make sure he does not receive any mail from Flyspray.

2. - Spam comment: Just delete the comment.
   - Spam task: Override the task description and task summary as it is not allowed to delete a task from Flyspray. (a feature that was made in early days) Then move the task to a //spam 'project'//. I see it as a waste bin for Flyspray tasks. Only admins have access to that.

3. Delete the spam user account

### Hacked User Account==

If I think the spam is from a hacked user account:

1. Disable user account and reach/phone the user if I know them (e.g. employees, customers)

2. - Spam comment: Delete or edit the comment.
   - Spam task: Edit task or move to //spam project// (waste bin)

3. Reenable/Edit user account if 1. is sorted out.


### Quick and Dirty

I you do not care to much about history/consistency and know SQL and have access to the database you can also brutal delete the offending comments and tasks of that user account from the database.
