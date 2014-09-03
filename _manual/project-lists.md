---
layout: manual
title: Project Lists
manual: proj
order: 10
---

*Lists* are those dropdown list items that you see on the task details page, and the new task page. They allow you to classify your tasks further by specifying things like *Task Type*, *Category*, etc. You can also [[searching tasks|search for tasks]], using content of Lists as search criteria. There are six project-level lists - *Task Types*, *Task Statuses*, *Resolutions*, *Categories*, *Operating Systems* and *Versions*.

Although the name of each of these lists is pre-defined, the items in the list are entirely up to you. If you want to use versions called *Apple*, *Orange* and *Banana* you can.

These lists give you a lot of flexibility. For example, if you design products for many different customers, you might use a project for each customer, and use categories to represent the different widgets you designed for each customer.

**Note:**  Lists can also be edited at global level (across all projects).  Members of the global *Admin* group can do this in the *Administrator's Toolbox*.  The dropdown box shown on the task details page will contain the items from the global list **and** the project list. Use the global list for common items which apply to all projects, and the project list for items specific to this project.

Shown at the bottom of this page is the Categories list editor for the Flyspray project. You can reach the Categories editor by selecting your project, clicking the Projects link in the admin menu, then Categories from the Project sub-menu.

  * **Name** is what appears in the dropdown list itself.
  * **Order** determines the order in which the names appear in the list. When you have list items defined at both global and project level, it is these numbers that are used for the sorting (lowest first) so if you want the global items to appear last, start numbering them from (say) 100 and use low numbers in your project-specific items. This field is not used for *Categories*.
  * **Show** determines if the category name should be shown in the list. Some categories may not be used by your project anymore, so you might like to hide them from view. Existing tasks using that list item will not change, as you haven't deleted the list item from the database, you are merely not showing it. When you edit a task, list items that are not shown will not appear in the categories dropdown list, so the category for that task will change if you save it.
  * **Delete** allows you delete unused list items. If any task (whether open or closed) is using that item, the delete box will be greyed out. You can only delete items which have never been used.

There are a few fields which apply only to the *Categories* list.

  * **Owner** This user will be notified when a new task is opened in that category.  If no owner is defined here, the project *Default Category Owner* will be notified instead.

  * **Sub-categories** You will notice that some lines are indented with arrows at the left of them. This is peculiar to Categories, and means that it is a subcategory of the left-aligned category above it. For example, the Translations category has sub-categories of Français, Español, Italiano, Deutsch and Polski. If a subcategory has no owner, then the parent category owner will be notified. If the parent category has no owner, then notifications go to the Default Category Owner, set in the Project Preferences.


<img src="/images/manual/categorylist.jpg" class="img-responsive" alt="category list">

### Adding New List Items

To add a new category, use the form at the bottom of the page. You can enter the name, order, select the category owner and if it is a sub-category.

The other lists (Task Types, Resolutions, Operating Systems and Versions) are similar to Categories, with the only difference being that there are no sub-items for those lists.

### Deleting List Items 
Flyspray only allows deleting of list items if they haven't been referenced in any tasks.  If a task refers to a list item and you delete it, there will be a blank field where that list item used to be.  Additionally, accurate reporting becomes next to impossible.  If you haven't referred to a list item in any tasks, then a "delete" checkbox will appear next to that list item.  To delete that item, tick the checkbox and click *Update*.
