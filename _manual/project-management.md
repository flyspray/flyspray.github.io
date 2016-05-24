---
layout: manual
title: Project Level Configuration
manual: proj
order: 1
---

Many Flyspray settings are managed at the Project level. To reach these settings, show the project you wish to manage, then click the *Manage Project* link on the menubar.  You will arrive at a screen similar to the image shown below.

<img src="/images/manual/projectoptions.jpg" class="img-responsive" alt="project options">

### Field descriptions 

Most options should be self-explanatory. More complicated ones are explained here.

#### General

<dl>
	<dt>Default Category Owner</dt>
	<dd>The user who gets notified when a new task is opened __if__ the category used for the task has no owner. Category owners are defined in the Category list for the project. This field can be left empty; if the category has no owner and there is no default owner, then no notification is sent.</dd>

	<dt>Introductory Message</dt>
	<dd>The text shown at the top of each project page. You could use it to show guidelines for bug submission, or simply for a Message Of The Day (MOTD).
	</dd>

	<dt>Default task description</dt>
	<dd>The default text for new tasks.</dd>

	<dt>Allow anyone to view this project</dt>
	<dd>Everyone (including anonymous users) can see this project. Without this permission, unauthorized users do not even get to see that the project exists. This setting allows everyone to see the project, but not the tasks in that project. Viewing of tasks is controlled by project/global permissions.
	</dd>

	<dt>Allow anonymous users to see tasks</dt>
	<dd>All users view tasks of this project without any further permissions.</dd>
	<dt>Allow anonymous users to open tasks</dt>
	<dd>Allows anonymous users to open new tasks in this project. Disabling this option means that only registered users with the "open new task" permission can open tasks.
	</dd>
</dl>

Look at [understanding permissions](/manual/understanding_permissions) to find out more.

### Look and Feel

<dl>
	<dt>Theme</dt>
	<dd>The colour scheme and layout for this project. See <a href="/manual/themes">Themes</a></dd>
	<dt>Default entry page</dt>
	<dd>You to choose which view is displayed when opening a project. Tasklist and roadmap should be clear, "top level view" is a little summary for the project, also called "overview".
	</dd>
</dl>

### Notifications 

<dl>
	<dt>Email address & Jabber ID</dt>  
	<dd>Where you can enter addresses to be notified when a task changes, and the events that trigger a notification.  Any address put in these fields will be notified when a new task opens, is modified, comments/files added, tasks closing etc.</dd>
	
	(2016-05-24 Note by peterdd: Noticed the feature was never completed. Now planned for FS1.1 with some refactoring required for this feature. See https://bugs.flyspray.org/1812 ) <del>If you want more than one address, separate them with a semicolon. This feature could be useful for a mailing list, or to ensure someone in particular is notified when they're not the default category owner.</del>
	

	<dt>Notification types</dt>
	<dd>Define exactly which events generate a notification.  Use the usual Ctrl and Shift combinations to select multiple types.
	</dd>
</dl>

 * If a user is already on the notification list to a task, their address will not be added again to the each notification sent out.

### Feeds

// todo
