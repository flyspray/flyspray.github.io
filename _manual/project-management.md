---
layout: manual
title: Project Level Configuration
manual: proj
order: 1
---

===== Project-Level Configuration =====

Many Flyspray settings are managed at the Project level. To reach these settings, show the project you wish to manage, then click the //Manage Project// link on the menubar.  You will arrive at a screen similar to the image shown below.

{{projectoptions.jpg}}


==== Field descriptions ====

Most options should be self-explanatory. More complicated ones are explained here.

=== General ===

**Default Category Owner** is the user who gets notified when a new task is opened __if__ the category used for the task has no owner. Category owners are defined in the Category list for the project. This field can be left empty; if the category has no owner and there is no default owner, then no notification is sent.

**Introductory Message** is the text shown at the top of each project page. You could use it to show guidelines for bug submission, or simply for a Message Of The Day (MOTD).

**Default task description** is the default text for new tasks.

**Allow anyone to view this project** lets everyone (including anonymous users) see this project. Without this permission, unauthorized users do not even get to see that the project exists. This setting allows everyone to see the project, but not the tasks in that project. Viewing of tasks is controlled by project/global permissions, and the next setting here ...

**Allow anonymous users to see tasks** lets all users view tasks of this project without any further permissions.

**Allow anonymous users to open tasks** simply allows anonymous users to open new tasks in this project. Disabling this option means that only registered users with the "open new task" permission can open tasks.

Look at [[understanding_permissions]] to find out more.

=== Look and Feel ===

**Theme/Style** selects the colour scheme and layout for this project. (See [[:themes]])

**Default entry page** allows you to choose which view is displayed when opening a project. Tasklist and roadmap should be clear, "top level view" is a little summary for the project, also called "overview".

=== Notifications ===

**Email address & Jabber ID**  is where you can enter addresses to be notified when a task changes, and the events that trigger a notification.  Any address put in these fields will be notified when a new task opens, is modified, comments/files added, tasks closing etc.  If you want more than one address, separate them with a comma or semicolon.  This feature could be useful for a mailing list, or to ensure someone in particular is notified when they're not the default category owner.

**Notification types** define exactly which events generate a notification.  Use the usual Ctrl and Shift combinations to select multiple types.

=== Feeds ===

Well, I guess this is about RSS feeds. If you know more, edit this section.

==== Technical Information ====
  * If a user is already on the notification list to a task, their address will not be added again to the each notification sent out.  Flyspray doesn't do duplicates if at all possible.