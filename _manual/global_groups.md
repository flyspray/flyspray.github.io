---
layout: manual
title: "Understanding Permissions: Global Groups"
manual: user
order: 20
---

Each Flyspray user is in exactly one global group. The group permissions in the global groups apply across all projects, so you should be careful when placing someone in a global group with more privileges. There are two ways to change which global group a user is in:

Through the global group manager
Click on the Users and Groups link in the Administrator's Toolbox.

<img src="/images/manual/globalgroupmanager.jpg" class="img-responsive" alt="Project Group Permissions">

To change which global group a user is assigned to, search for the users name in the edit user field. Then choose another group from the drop down list in global group, and click update details button. Flyspray processes the request, then shows a green statusbar with a "success" message at the bottom of the page.

Remember, the permissions for the global groups are applied across all projects. If you don't want someone to have the ability to change all tasks in all projects, then don't place them in a global group with that permission. You should take care to limit how many users are in the global Admin group. Ask yourself if they really do need access to all of Flyspray's options, or if they only need lesser permissions at the project groups. Giving users the lowest permissions that they need for their respective jobs is considered good security practice.

To see or change the permissions in a particular group, select the group from the edit group field to be taken to the Edit Group page. You can also see the users currently assigned to the group.