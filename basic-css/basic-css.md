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

---

## Use a CSS Class to Style an Element

Use classes to add resuable styles across HTML elements.
A common case is where we don't want *all* `h2` elements to be red.
Create a class and all elements with the specified class will use it's declarations.

```html
<style>
  .red-text {
    color: red;
  }
</style>

<h2 class="red-text">CatPhotoApp</h2>
```
Note: all CSS classes start with `.` e.g. `.red-text`.
But we omit the `.` when the HTML element is referencing the class.

---

## Use an id Attribute to Style an Element

Like classes, they can be used to style with CSS.
An `id` is not resusable, it can only be used on a single element.
However it does have a higher importance than a class; if an element has an `id` and a `class` then the `id` declaration will take priority.
When specifying an `id` declaration in the CSS, start them with a `#`

```html
<style>
  #cat-photo-form {
    background-color: green;
  }
</style>
```

---

## Adjust the Padding of an Element

Elements are essentially recangles on a canvas.
There are three important elements that can be used to control the space around an element; `padding`, `margin` and `border`.

`padding` controls the space between the elements content and the border

```html
<style>
  .injected-text {
    margin-bottom: -25px;
    text-align: center;
  }

  .box {
    border-style: solid;
    border-color: black;
    border-width: 5px;
    text-align: center;
  }

  .yellow-box {
    background-color: yellow;
    padding: 10px;
  }

  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 10px;
  }
</style>
<h5 class="injected-text">margin</h5>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```
![element with 10px padding][element_10_padding]

```html
<style>
    .blue-box {
    background-color: blue;
    color: #fff;
    padding: 10px;
  }
</style>
```
![element with 20px padding][element_20_padding]

---

## Adjust the Margin of an Element

An elements `margin` property controls the space between it's border and the elements surrounding elements.

```html
  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: 20px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
   
   padding: 20px;
    margin: 10px;
  }
```

Note how the red box appears smaller due to it's greater margin value.

![margin 20][margin_20]


```html
  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: 10px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
    margin: 10px;
  }
```
![margin 10][margin_10]

---

## Add a Negative Margin to an Element

An element can *grow* larger by changing it's `mwrgin` to a negative value.

```html
  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: -15px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
    margin: 10px;
  }
```
![margin -15][margin_-15]

---

## Add Different Padding to Each Side of an Element

Padding can be assigned different values to different sides of an element using;
 - `padding-top`
 - `padding-right`
 - `padding-bottom`
 - `padding-left`

```html
   .red-box {
    background-color: crimson;
    color: #fff;
    padding-top: 40px;
    padding-right: 20px;
    padding-bottom: 20px;
    padding-left: 40px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding-top: 40px;
    padding-right: 20px;
    padding-bottom: 20px;
    padding-left: 40px;
  }
```

![padding 40 20][padding_40_20]

---

## Add Different Margins to Each Side of an Element

As with `padding` define a value to each side of the element's `margin` using the selectors `margin-top`, `margin-right`, etc.

```html
  .blue-box {
      background-color: blue;
      color: #fff;
      margin-top: 40px;
      margin-right: 20px;
      margin-bottom: 20px;
      margin-right: 40px;
  }
```

---

## Use Clockwise Notation to Specify the Padding or Margin of an Element

Specify all the values using a one-liner; `padding: 10px 20px 10px 20px;`

```html
  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 40px 20px 20px 40px;
  }
```

```html
  .blue-box {
    background-color: blue;
    color: #fff;
    margin: 40px 20px 20px 40px;
  }
```

---

## Use Attribute Selectors to Style Elements

Specify all elements where the attribute `type` has the value `radio`

```html
  [type='radio'] {
    ...
  }
```

---

## Absolute vs. Relative Units

So far we've used `px` this is a fixed measurement, absolute.

A relative unit value sets the measurement relative to another value. For example `em` sets the value relative to the elements `font-size`. 
Note; when using `em` to set the size of a `font-size` the parent elements `font-size` is used for the relative measurement.

```css
  .red-box {
    background-color: red;
    margin: 20px 40px 20px 40px;
    padding: 1.5em;
  }
```

---

## Inheriting Styles

Define some definitions for the `body` element;

```css
  body {
    background-color: black;
    color: green;
    font-family: monospace;
  }
```

Now when a `h1` element is added, it will **inherit from** the `body` definitions because the `body` and `h1` have a **parent -> child** relationship.

```html
<body>
  <h1></h1>
</body>
```

Every element defined inside the `body` element will inherit from `body`.

## Overriding Styles

Define a class which we'll apply to the `h1`;

```css
  .pink-text {
    color: pink;
  }
```

```html
<body>
  <h1 class="pink-text"></h1>
</body>
```

Even though the `color` attribute is still inherited from `body` the `pink-text` takes priority.

Like class inheritence in programming; a member defined for the class will override an inherited member.

What if we gave `h1` two class declarations?

```css
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
```

```html
<body>
  <h1 class="pink-text blue-text"></h1>
</body>
```
**The text colour will appear blue because `blue-text` appears last in the css declarations.**

The order in which the classes appear in the `html` is unimportant.

Now let's add `id` into the mix.

```css
  #orange-text {
    color: orange;
  }
```

```html
<body>
  <h1 class="pink-text blue-text" id="orange-text"></h1>
</body>
```

**The text colour will appear orange as an `id` overrides any/all `class`.**

It's possible to override `id` declarations with *inline styles*.

```html
 <h1 class="pink-text blue-text" id="orange-text" style="color: white;"></h1>
```

**The text colour will appear white as an inline style overrides `id` and `class`.**

There is an all-powerful way to override any styling made to an element, using `!important`;

```css
  .pink-text {
    color: pink !important;
  }
```

**!important overrides any/all other styling declarations.**

---

## Hex Color Codes

Define colors with hex codes instead of their named values, allowing for a vast range of colors to work with.

```css
  body {
    background-color: #000000;
  }
```

There are approx 16 000 000 colors to choose from;

```css
.red-text {
    color: #FF0000;
  }
  .green-text {
    color: #00FF00;
  }
  .dodger-blue-text {
    color: #1E90FF;
  }
  .orange-text {
    color: #FFA500;
  }
```

Abbreviate hex codes using three-characters;

```css
.red-text {
    color: #F00;
  }
  .fuchsia-text {
    color: #F0F;
  }
  .cyan-text {
    color: #0FF;
  }
  .green-text {
    color: #0F0;
  }
```

Browser interprets `#F00` as `#FF0000`, `#F0F` as `#FF00FF` provides a slimmed down palette but is a lot easier to remember!

[Hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal)  
[RGB Color Model](https://en.wikipedia.org/wiki/RGB_color_model)

--- 

## RGB Color Codes

Define color using a 3 item set of 3 digits, representing red, green, and blue.

```css
  body {
    background-color: rgb(255, 165, 0);
  }
```

The limit for each color set is 0 - 255, meaning there are the same number of color combinations as available in the hex system (above).

```css
.red-text {
  color: rgb(255, 0, 0);
}
.orchid-text {
  color: rgb(218, 112, 214);
}
.sienna-text {
  color: rgb(160, 82, 45);
}
.blue-text {
  color: rgb(0, 0, 255);
}
```

[element_10_padding]: ./assets/element_padding_01.png
[element_20_padding]: ./assets/element_padding_02.png
[margin_20]: ./assets/margin_20.png
[margin_10]: ./assets/margin_10.png
[margin_-15]: ./assets/margin_-15.png
[padding_40_20]: ./assets/padding_40_20.png 