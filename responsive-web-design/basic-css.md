# Basic CSS

## Introduction

CSS allows the developer to control;
 - colour
 - fonts
 - positioning
 - spacing
 - sizing
 - decoration
 - transition

There are 3 ways to apply CSS;
 1. Directly to the HTML element using the `style` attribute
 2. Using `<style>` in the HTML document
 3. Externally, then reference the .css file in the HTML document

Option 3 is the preferred method as it seperates content and style.
It also allows the style to be changed without modifying the content and structure specified by the HTML file.

With CSS a HTML element in the DOM (Document Object Model) is targetted and a variety of it's attributes are changed.

---

## Change the Color of Text

Use an elements `style` attribute to change it's color.
Note the `;` when closing the string attribute, this is good practice.

This is an example of basic inline CSS.

```html
<h2 style="color: red;">CatPhotoApp</h2>
```

---

## Use CSS Selectors to Style Elements

Imagine having to do that 👆 for *each* HTML element, large projects would soon become unmanagable.
Luckily we can use a `<style>` block and specify attributes for HTML elements like `h2` using selectors.

```html
<style>
  h2 {
    color: blue;
  }
</style
```
Note the syntax of the style block, each selector is opened and closed with braces.

