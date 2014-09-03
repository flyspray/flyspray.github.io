---
layout: manual
title: "Understanding Permissions: Project Groups"
manual: user
order: 30
---

## Overview 

Imagine for a minute that you do not want developers from other projects to modify your project's tasks, or that you want to completely hide your tasks from everyone except your own project's developers. This is where project permissions are used. To get to the Project-level Groups page, click *Manage Project*, then the *User Groups* link in the Project Manager's Toolbox.  Members of the global *Admins* group should ensure that they are in the PM Toolbox, and not the Admin Toolbox, as they might accidentally start assigning permissions across all projects!

Through the [project management](/manual/project-management/) interface, you can disable the ability for "anyone" to view your project, then use the groups described on this page to add individual users to your project.

Every new project has a Project Managers (PM) group automatically created. Members of the PM group can modify project preferences, as well as group assignments and permissions. Clearly you do not want all your developers to be able to do this, so it would be wise to create more groups with varying permissions for your project members. To add a new group, simply click the Add new group link near the top of the page. You will be taken to a simple page where you can add a group name, description, and set the member permissions. 

After adding your new project-level group, you will be returned to the Project users and groups page. To add users to your new group, scroll down to the bottom of the page to find the users not currently assigned to a group in your project. Highlight multiple users by holding down your computer's Ctrl key while clicking their names, select (from the drop-down list) which group you want to add them to, and click Add users to group. Flyspray processes your request, and returns a green status bar with the result. You should now have users in your project-level group.

Now look at the users in your new group; each one will have a checkbox next to their name.
Underneath each group's users is a button and a drop-down list. To change which group you want a user in, check the box next to their name, select a group from the drop-down, and click the Move users to group button. To remove the user from your project entirely, simply use the No group - remove from project option in the drop down.

**Note:** While [global groups](/manual/global_groups/) assign permissions across all projects, project-level groups assign permissions to one project only. Only Global Admins and Project Managers may change project level groups, and Project Managers may not change other projects groups.

### Technical Information

Flyspray stores global and project-level groups in the same database table. To determine which group is associated with which project, the project_id is stored in the **{$dbprefix}_groups.belongs_to_project** field. If the group is global, Flyspray stores zero (0) in that field.