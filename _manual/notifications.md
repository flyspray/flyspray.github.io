---
layout: manual
title: Notifications
manual: tasks
order: 90
---

Sometimes you need to know what is happening with a task, even if you're not the one currently working on it. That is where notifications are helpful.  To receive a notification when a task has been modified or had something added to it, click the *Watch this task* button beneath a task's details.  Later if you decide that you no longer want to be notified about changes to a particular task, click the *Stop watching this task* button.

### The Notifications Tab 

**Note:** This paragraph describes functionality that can only be accessed by the Project Manager or a member of the global Admin group.

<img src="/images/manual/notifytab.jpg" class="img-responsive" alt="Notification Tab">

Shown is a list of users who are currently "watching" this task. When anything changes in the task (task details modified, comments or attachments added etc), Flyspray sends out a short notification message to each person on the list, letting them know what the changes or additions are. Notifications are sent using email or [Jabber instant messaging](http://www.jabber.org), using the email/jabber address in each user's profile. Usually each user can choose their preferred method of notification, but it can be over-ridden in the global options dialog. Users should ensure that the notification addresses in their profile are correct, as Flyspray will not complain if they are wrong.

To add a user to the notification list for a task start typing there name in the 'Add user to this list' field, and click the *Add* button.  To remove a user, click the *Remove* link next to their name.


### Tips 
  * Notifications are by default not sent to the user making the change.  The user already knows what action they made, so Flyspray doesn't fill their inbox with information they already know. This behavior can be changed by the user on his profile page.
  * Notifications are **always** sent to the person who has been assigned the task, regardless of whether they are on the task's notification list or not.


### Technical Information 

**Adding to notification list:**  The dropdown list for adding users to the notification list does not contain every user registered on your Flyspray installation.  The list only contains users who are members of your [Project groups](/manual/project_groups), as well as users in [global groups](/manual/global_groups) defined as "can be assigned tasks" in the [[global options]].  This is done by the ListUsers() function, in `includes/functions.inc.php`

**Database tables:**  Users to be notified are listed in the **{$dbprefix}_notifications** table.

**Standard Notification Triggers:**  These are the times when a notification is sent to those on a task's notification list:
  * Task details changed
  * Task closed
  * Task re-opened
  * Dependency added
  * Dependency removed
  * Comment added (adding a note if any files were attached)
  * Related task added
  * Taken ownership (user assigned a task to themself)
  * New assignee. If a user is assigned a task, so they need to know.

**Special Notification Triggers:**
  * New task opened (category owner is notified)
  * Someone requested a Project Manager to action something on a certain task.  These notifications are sent to everyone in the project who is in a group with the *Manage Project* permission.
  * Project Manager denied request.  If a PM denies the above request, everyone on the notification list receives the notification.
  * Sending a confirmation code for a new user signup.
  * Sending a user a "magic URL" so that they can change their password.
