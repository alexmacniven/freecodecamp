# Basic HTML and HTML5

## Introduction

HTML describes the structure of a webpage.
Using a special syntax it gives informs the browser about the data.

HTML uses tag based notation to achieve this;
```html
<h1>this is a heading</h1>
<p>this is a paragraph</p>
<ol>
    <li>this is a list item</li>
    <li>so is this</li>
</ol>
```
HTML born out the early www use case.
Pages were documents with links to other documents.

W3C ensures HTML standardisation.

---

## Say Hello To HTML Elements

Most HTML elements have an opening and closing tag.
These tags surrond a piece of data, thus the tags add context to the data.
E.g.
```html
<p>this is a piece of textual data.</p>
```
In the above example, `<p>` is the opening tag and `</p>` is the closing tag

### Solution
<h1>Hello World</h1>

---

## Headline with the `h2` Element

Headlings help give structure to web pages.
They should generally be used in order, 1 through to 6.
It's common practice for `h1` to be used for main headings and `h2` to be used for sub-headings.

### Solution

```html
<h1>Hello World</h1>
<h2>CatPhotoApp</h2>
```

---

## Inform with the Paragraph Element
P
The `<p>` tag is used to inform the browser of a paragraph.
It is the *preferred* element for standard text data.

### Solution

```html
<h1>Hello World</h1>

<h2>CatPhotoApp</h2>

<p>Hello Paragraph</p>
```

---

## Fill in the Blank with the Placeholder Text

Since the dawn of the internet and www, *lorem ipsum* text has been used a placeholder for text.

### Solution

```html
<h1>Hello World</h1>

<h2>CatPhotoApp</h2>

<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
```

---

## Comment and Uncomment HTML

Commenting offers a convinent method of leaving messages for yourself or other developer.
In html, comments are opened with `<!--` and closed with `-->`

### Uncomment HTML Soltion

```html
<!--
    Comment tags have been removed!
-->
<h1>Hello World</h1>

<h2>CatPhotoApp</h2>

<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
```

### Comment HTML Solution

```html
<!--
<h1>Hello World</h1>
-->
<h2>CatPhotoApp</h2>
<!--
<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
-->
```

---

## Delete HTML Elements

Be sure to remove both the opening and closing tag, otherwise the markup will make no sense!

### Solution

```html
<h2>CatPhotoApp</h2>

<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
```

---

## Introduction to HTML 5 Elements

HTML5 introduced more descriptive tags.
These included;
 - main
 - header
 - footer
 - nav
 - video
 - article
 - section

Some of these can be used to aid the structure of an HTML document.
They can also optimise a web page for SEO, as well as help other developers find specific pieces of the document.

### Solution

```html
<h2>CatPhotoApp</h2>
<main>
    <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
    <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

---

## Add Images to your Website

Image tags are an example of a self closing tag.
All image tags must have an `alt` attribute, unless they are purely decorational.

### Solution

```html
<h2>CatPhotoApp</h2>
<main>
  <img src="https://bit.ly/fcc-relaxing-cat", alt="A really chilled out cat.">
  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

---

## Link to External Pages with the Anchor Element

The `<a>` tag is used to link to external content.
An anchor tag needs a `href` attribute describing the path to the content.
And should also have a textual componenent.

### Solution

```html
<h2>CatPhotoApp</h2>
<main>

  <a href="http://freecatphotoapp.com">cat photos</a>

  <img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

---

##  Link to Internal Sections of a Page with the Anchor Element

Anchor tags can be used to reference internal content with the help of `id` attributes.
The `href` element of the anchor tag should start with a `#` and then the `id` attribute value of the element we're linking to.
Understandably the element we're linking to needs an `id` attribute with a corresponding value.


The `target` attribute of an `a` element describes how to open the content.
`target="_blank"` will open the content in a new tab.

### Solution

```html
<h2>CatPhotoApp</h2>
<main>

  <a href="#footer">Jump to Bottom</a>

  <img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff. Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched. Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched. Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff. Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
  <p>Meowwww loved it, hated it, loved it, hated it yet spill litter box, scratch at owner, destroy all furniture, especially couch or lay on arms while you're using the keyboard. Missing until dinner time toy mouse squeak roll over. With tail in the air lounge in doorway. Man running from cops stops to pet cats, goes to jail.</p>
  <p>Intently stare at the same spot poop in the plant pot but kitten is playing with dead mouse. Get video posted to internet for chasing red dot leave fur on owners clothes meow to be let out and mesmerizing birds leave fur on owners clothes or favor packaging over toy so purr for no reason. Meow to be let out play time intently sniff hand run outside as soon as door open yet destroy couch.</p>

</main>

<footer id="footer">Copyright Cat Photo App</footer>

```

---

## Nest an Anchor Element within a Paragraph

It's common to nest links within blocks of texts.
Make sure your tags are closed in the correct order, first-in-last-out.

### Solution

```html
<h2>CatPhotoApp</h2>
<main>

  <p>View more <a href="http://freecatphotoapp.com" target="_blank">cat photos</a></p>

  <img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

---

## Make Dead Links Using the Hash Symbol

Useful for working with the site in development, but pretty important when using Javascript to change the behaviour of an anchor. 

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#" target="_blank">cat photos</a>.</p>

  <img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>

```

---

## Turn an Image into a Link

Just like using a textual element as an anchors text in section [Nest an Anchor Element within a Paragraph](#nest-an-anchor-element-within-a-paragraph), it's also possible to use an image.

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```