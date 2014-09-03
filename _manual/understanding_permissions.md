---
layout: manual
title: "Understanding Permissions: Global and per-project"
manual: user
order: 10
---

## Understanding Permissions 
Flyspray allows you to set permissions on a "global" level and on a per-project level. 
There are many relatively fine-grained permissions that can be set, for example "View comments", and "Assign others' tasks to self".  

As is customary in many online systems, to avoid setting these for every individual user, instead permissions are set for groups of users. Some default groups are provided, and you can add your own. 

Functions for this area are accessed through the Users and Groups panel. 

For global groups: Admin Toolbox -> Users and Groups. 

For project groups, select the project and then Manage Project -> User Groups. 

Groups pertain either to the global level and their permissions apply globally, or they pertain to a single project, and apply just to that project. 

As you might have concluded, groups are not completely general. You cannot create a group that provides privileges for two specific projects, but of course you could create similar groups in each project. Instead it is perhaps better to think of "groups" as more like global and project "roles".

Once a group is available, you can add existing users to the group: Select Edit user, then select a group. A user can only be a member of one global group, and one group in each project.

You can edit the exact permissions that a group provides using the Edit Group feature, which presents a dialog like this:

<img src="/images/manual/projectgrouppermissions.jpg" class="img-responsive" alt="Project Group Permissions">

This same editability is available for global and project groups, through their respective Users and Groups panel.

### How permissions are combined

Flyspray combines the permissions that a user has at each level by OR-ing them together. If either level permits the user to do something, then permission is granted. Conversely, to deny permission to do something, the user's permissions in both their global and project groups must be set to "NO".

This probably leads to two main ways of using the groups and permissions apparatus:

**Global Only:**  Set all permissions using global groups, ignore project groups: this would be good where there's no pressing need for some users to have different permissions for different projects.

**Minimal global defaults + specific permissions using groups:** In this case, the most important permissions are set via groups, and most permissions at the global level are set to "NO". This would suit the situation where there are distinct groups of users dealing primarily with their own projects, with reduced or no need to access other projects' data.

