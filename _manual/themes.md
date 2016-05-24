---
layout: manual
title: Themes
manual: proj
order: 30
---

While many web applications rely upon complex templating to achieve different visual styles, Flyspray uses CSS standard to achieve different layouts and colours.  Almost anything can be achieved using CSS, just look at the [CSS Zen Garden](http://www.csszengarden.com) for examples and inspiration.

## CleanFS
The default Flyspray theme is 'CleanFS'.  It has a basic layout with a colour scheme that won't hurt your eyes.

<img src="/images/manual/cleanfs.jpg" class="img-responsive" alt="CleanFS theme">

## Extending the Default CleanFS Theme
Flyspray 1.0 comes with the CleanFS theme. You can extend the theme for each project by choosing a custom_yourname.css on the project settings page of a project or global Flyspray setting page. A custom_example.css is included.

Because the theme.css for the CleanFS contains also some CSS3 logic and some template files also contain php logic, it is recommended to use the CleanFS to be easy upgradable and do any customization by Flyspray settings and overwriting CSS styles with custom_*.css files in the CleanFS directory.

Almost all elements in Flyspray have **id** or **class** tags. For instance the body-tag: 
```html
<body class="pm p3" onload="">
```
In this example class **pm** is for every project setting page.
And class **p3** for project_id 3. So to change the background color of the header bar on all pages of **project 3** you could add
```css
body.p3 h1{background-color:#600;background-image:none;}
```
to change the top header bar background (currently the h1-tag) from default gray gradient to a dark red.

You can read which element has which tag by viewing the source code on a Flyspray page or by using:
  * web developer tools in Chrome (F12)
  * Firebug or builtin inspector (CTRL+SHIFT+c or F12) in Mozilla Firefox
  * DOM Explorer in Internet Explorer (F12)
  * or developer tools in Opera (CTRL-SHIFT+i)

## Creating your own theme 
If you really, really would like to create your own full theme (not recommended!), copy the `/themes/CleanFs` directory to `/themes/YourThemeName`. From there, open `/themes/YourThemeName/theme.css` and start editing.

**Before starting hacking your own full theme, ask peterdd how to easiest modify a custom_*.css file to get the effect you want**

Hint for Flyspray1.0: An alternative way is to stay with the CleanFS theme, make a copy of CleanFS/theme.css and replace 'theme.css' in CleanFS/templates/header.tpl with your customized theme.css filename.
This way the template files in CleanFS stay upgradable and you must only check if the default CleanFS/theme.css contains some logic changes like pure CSS tabs or CSS toggles. Maintaining different theme directory structures is too much work.

Keep in mind to use tpl_form() instead of just '<form action...>' for any database-changing html form, because this takes care of adding the anticsrf-token for you. Also db changing ajax requests must send the right token.

## Submitting your theme to us
While you are free to create themes for your own use, we would love for you to show us your work.  Contact us on our [mailing list](/community/mailing-list/) and show the world what you've done. Please don't send files to the mailing list, use Github instead.  If you would like us to host your theme on the [download](/docs/download) page, please let us know.  We can arrange to get it from you outside the mailing list.
