---
layout: manual
title: Coding Style
manual: cont
order: 20
---

# Flyspray code style

Basically we use PSR-12 https://www.php-fig.org/psr/psr-12/ for new Code with following exceptions or added rules:

### Indentation

We use **tabs** instead of the 4 spaces for indenting.

### Variables

* Use only English for variable names.
* Give variables a matching meaning, not too long, not too short.

* camelCase functions for PHP (they are case insensitive, so nothing breaks, but prefered format)
* lowercase new introduced variables for PHP (they are case sensitive!)

## PHPdoc

Use phpdoc syntax if you want document functions or classes.

## HTML and Templates

### input and label tags

Always **put the label tag behind their input tag** on the same level. Use the for-attribute to connect label with the input's id attribute.

Example:

```html
<input type="text" name="fieldname" id="fieldname" placeholder="placeholdertext"/>
<label for="fieldname">Field name</label>
```

This way the label can adapt to state and changes of the input element by pure CSS like :focus, :placeholder :required :invalid
The real visual appearance on the page can be changed by CSS, so the the label might also appear before input if appropriate.


**Do not** wrap the input in the label!

**Do not** put the label before the input in the HTML templates!

