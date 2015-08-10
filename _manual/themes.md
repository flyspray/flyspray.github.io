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

## Other themes
Flyspray only comes with the CleanFS theme. Other available themes can be downloaded from the [download](/docs/download) page.  To install a theme, extract it from the compressed archive into Flyspray's themes directory.  Then go to the [Project Manager's Toolbox](/manual/project_management), select it and save preferences.

## Creating your own theme 
If you would like to create your own theme, copy the `/themes/CleanFs` directory to `/themes/YourThemeName`.  From there, open `/themes/YourThemeName/theme.css` and start editing.

Hint for Flyspray1.0: An alternative way is to stay with the CleanFS theme, make a copy of CleanFS/theme.css and replace 'theme.css' in CleanFS/templates/header.tpl with your customized theme.css filename.
This way the template files in CleanFS stay upgradable. Maintaining different theme directory structures is too much work.

Almost all elements in Flyspray have id or class tags. You can read which element has which tag by viewing the source code on a Flyspray page or by using:
  * web developer tools in Chrome (F12)
  * Firebug or builtin inspector (CTRL+SHIFT+c or F12) in Mozilla Firefox
  * DOM Explorer in Internet Explorer (F12)
  * or developer tools in Opera (CTRL-SHIFT+i)

## Submitting your theme to us
While you are free to create themes for your own use, we would love for you to show us your work.  Contact us on our [mailing list](/community/mailing-list/) and show the world what you've done.  Please don't send files to the mailing list use Github instead.  If you would like us to host your theme on the [download](/docs/download) page, please let us know.  We can arrange to get it from you outside the mailing list.
