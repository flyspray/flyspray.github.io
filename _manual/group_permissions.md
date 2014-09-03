---
layout: manual
title: "Understanding Permissions: Group Permissions"
manual: user
order: 40
---

Because Flyspray has both global and project-level groups, a user's permission for a certain area can sometimes get a little blurry.

## Overview

For the mathematically minded, I'll get to the point - global permissions are boolean OR'ed with project-level permissions.

What this means to the rest of us is that if a particular global permission is NO, and the same project-level permission is YES, then the user's permission for that project is YES. Likewise, if the global permission is YES, and the project-level permission is NO, then the effective permission is YES.

If either the global permission or the project-level permission is YES, then the result is YES for that project.

Shown is an image of the permissions page for the Flyspray project's Contributors group; notice that some of the options are not selected. However, if those same options are selected in the user's global group, then they will have those rights regardless of what you select here.  Users can see their permissions for any given page by clicking the *Show Permissions* link at the top of the page.

## Technical Information 
Flyspray stores global and project-level groups in the same database table.  To determine which group is associated with which project, the project_id is stored in the **{$dbprefix}_groups.belongs_to_project** field.  If the group is global, Flyspray stores zero (0) in that field.