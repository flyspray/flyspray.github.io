---
layout: manual
title: "User Management: Enrollment and details"
manual: user
order: 1
---

### User Management

Only Administrators have the ability to manage other users. This means that you need to be a member of the global Admin group in order to do anything described on this page for other users, although you can edit some of your own details. This page describes how to edit user's details. If you are searching for information on changing user's permissions, please visit the [Group Permissions](/manual/group_permissions) page.


### Editing User Details

To edit a user's details, click *Admin Toolbox* from the menubar to take you to the Administrator's Toolbox.  From there, click *Users and Groups* to get to the group manager, type the username in the *Edit user* box and click *Edit*. The user you want to edit may be in any of the global groups shown. Flyspray does not yet have a "user search" tool, so you will need to know the username of the user you want to edit. Auto-completion will help you, as long as you know the first few letters of the username.

**Tip:** You can also edit any user by clicking their name on a task details page. 

There are a number of fields that you can modify.  *Email Address* is only required if the user wants to receive notifications by email. *Jabber ID* is only required if the user wants to receive notifications in their Jabber client. Note: You are required to fill in the *Real Name* field, and at least one of the *Email Address* and *Jabber ID* fields, otherwise Flyspray will not save the changes.

Notify Type is how the user wishes to receive notifications about changes to tasks they watch. Flyspray doesn't perform a sanity check on this field. If you select Email, but haven't entered an email address, then the user won't receive their email notifications!

*Date Format* is a personalised way of viewing the various dates shown in Flyspray. If you don't like the default date format, you can enter characters that make Flyspray change it. The same applies for *Detailed Date Format*, which is shown in other parts of Flyspray (eg. the task details page).

  * Flyspray 0.9.8 and newer versions use the PHP [strftime](http://php.net/strfatime) function instead, which is more flexible and supports locale-specific dates, but which uses different format strings.

Users without Admin permissions cannot edit the next two fields - *Global Group* and *Account Enabled*. Unchecking the *Account Enabled* box will disable the user's account, and immediately log them out. Learn about global groups on the [global groups](/manual/global_groups) page.

To change a user's password, simply type a new one into the *Change Password* field, and the same one again into the *Confirm Password* field.

When you have finished editing, click the Update Details button to save your changes.

### Adding a new user 

If a user cannot create a new account, you might like to create one for them. Navigate to the *Users and Groups* manager as described above, and click *Register New User*. The same rules described above in Editing User Details also apply when adding a new user. You must fill in all fields, but you can fill in either Email Address or Jabber ID. Note: Be careful which global group you put the user in. The default global group is Admin.
