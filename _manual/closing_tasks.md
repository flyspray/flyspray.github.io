---
layout: manual
title: Closing Tasks
manual: tasks
order: 110
---

If you have the permission to close a task, a close task button is shown on the task details page. It popups a form, where you can select a closing reason and insert an optional comment.

By default the task progress is set to 100% unless you deselect that option.

<h3>Special close reasons</h3>

<h4>Duplicate task</h4>
See [Related Tasks](/manual/related_tasks) section of the manual

<h3>Deleting tasks</h3>

It is not possible to delete a task direct. This is a an explicit design decision made by the creators many years ago 
to keep possible QA-staff happy in companies. (Editor: if I understand the discussions right on bugs.flyspray.org)

In case that things went really wrong due something like a spambot or someone vandalized and created many tasks without solid reason, here is a workaround for admins: Create a new empty project, move the bad tasks to this project, delete the project. Or just let this project be the graveyard project if it doesn't contains thousands of silly generated tasks.
