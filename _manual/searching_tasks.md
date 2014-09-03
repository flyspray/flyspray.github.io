---
layout: manual
title: Searching Tasks
manual: tasks
order: 10
---

When you have a lot of tasks on your Flyspray, you may have trouble locating a certain task by visual scanning alone.  This is where you may find the *Search* functionality useful.

### Overview
Return to the task list using the *project selector*.  In the CleanFS theme (default), you will see a search bar similar to the image below when you expand advanced.

<img src="/images/manual/searchbar.jpg" class="img-responsive" alt="Searchbar">

From here you can enter some search terms, and select different options to narrow your search criteria.  Click *Search* to send your search to Flyspray for processing.  The page will reload with a new tasklist matching your search criteria.

### Search criteria

All fields are straightforward with a couple of exceptions that might need a little clarifying.

#### Status
This field defaults to "All open tasks", and as such, will return all tasks that are not marked "closed".  This means that they may have any status, as long as they are still marked "open".   Another option is "all statuses", meaning that Flyspray will return all tasks regardless of whether they are open or closed.  It is always a good idea to search the tasklist using the "all statuses" option before opening a new bug report or feature request.  Your bug may have been already fixed, or your feature request already implemented, and the tasks closed.


### Technical Information
**Assigning tasks:**  The dropdown list that appears at the *Assigned To* field does not contain every user registered on your Flyspray installation.  The list only contains users who are members of your [Project groups](/manual/project_groups), as well as users in [global groups](/manulal/global_groups) defined as "can be assigned tasks" in the [global options](/manual/global_options).  This is done by the `ListUsers()` function, in `includes/functions.inc.php`

**Due Date:** Searching by due dates only returns tasks with a number greater than zero (0) in the **{$dbprefix}_tasks.due_date** field.  Therefore, if a task doesn't have a due date set, it will not be included in the query.