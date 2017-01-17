---
layout: manual
title: Private Tasks
manual: tasks
order: 50
---

Although you are able to deny anonymous users the ability to view tasks, often this isn't enough. Sometimes you want to allow members of your project the ability to view most tasks, but to hide tasks of a sensitive nature (such as security-related).


### Overview
Project Managers can mark a task private simply by clicking the *Make Private* button on a task details page. Once that is done, the task can only be viewed by the following people:

* Administrators
* Project managers
* The user who opened the task
* Anyone assigned to the task

Project Managers have the ability to view all tasks in their project, regardless of privacy settings.

**Note:** Members of the global *Admin* group have Project Manager permissions across all projects, and they will be able to see your private tasks. The default settings for the *Developer* group also includes Project Manager permissions, so members of this group will also be able to see all private tasks.

### Technical Information
The *Make Private* button simply toggles the **{$dbprefix}_tasks.mark_private** field in that particular task's table row.  Zero (0) = public, one (1) means private.
