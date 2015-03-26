---
layout: manual
title: Coding Style
manual: cont
order: 20
---

Coding Style
============

Before starting
---------------

I am pretty certain that setting too narrow code style rules just leads to chaos... The reason being that if the rules are too strict, none will ever follow 100% of them, resulting in non respected code style chart. That's why there will be no more PSR-2 or 3.

That being said, you will soon find here a complete list of our requirements. These are basic rules that you have to follow. We won't merge any commit not respecting these few  rules!


Flyspray code style
-------------------

# Identation

* You will use tabs to correctly ident your code. Spaces are only authorized to fine tune your identation in case of multiline if statements per exemple
* Childs must be correctly ident to their respective parents, and that is for any language, php of course, but html, css, javascript of any other languages FS is or will use.

# variables

* Use english only for variables
* Name your variables correctly. Their name must be in direct relation to their use
* We follow the camelCase convention
``` php
<?php

// Variable that will hold the shoe size of your customer
$customerShoeSize

// Invalid forms
$customer_shoe_size;
$CustomerShoeSize;
$Customer_Shoe_Size;
$customershoesize;
?>
```

More to come, under work.