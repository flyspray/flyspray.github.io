---
layout: manual
title: Dependencies
manual: tasks
order: 40
---

Flyspray can have tasks that depend upon other tasks. Basically what this means is that if task #1 depends upon task #2, you cannot close #1 until #2 is closed. The image below shows the dependencies block.

<img src="/images/manual/dependencies.jpg" class="img-responsive" alt="Task Dependencies">

### Overview
Under the task description you can see the tasks that this task depends upon. The line through some tasks indicates that they have been closed. The tasks without a line through them are stopping this task from being closed. In fact, the button to close a task will be grayed out until all dependencies are closed. Simply close all the tasks that this task depends upon, and you can then close this task.

To add another dependency click on Quick Actions > Associate dependent task, enter the task id in the text field, and click the "Add" button. Note: Flyspray will not let you create a dependency back to the same task, nor can you create a dependency of a task that this task is blocking. If you did that, you would never be able to close some tasks! If you receive an error when you try and add a dependency, this is probably why.

### Permissions
To add or remove dependencies, you need to have permission to edit the current task. This means that you need to meet one of the following two criteria:

  * If the task is assigned to you, be a member of a group with the *Modify Own Tasks* permission, or
  *  Be a member of a group with the *Modify Other Tasks* permission.

