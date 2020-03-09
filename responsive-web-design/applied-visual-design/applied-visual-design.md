# Applied Visual Design

## text-align

Controls how text is aligned in it's element.

`left`, `right` and `center` work as expected.

`justify` makes all lines except the last meet the left and right edges of the element.

```css
    text-align: center;
```

## width

`width` values can be supplied as relative (`em`), absolute (`px`) or as a percentage of it's containing parent.

```css
img{
  width: 220px;
}
```

## height

Likewise, with the `height` element property.

```css
h4{
    height: 25px;
}
```

## strong (bold)

Wrap text in `<strong>` tags to apply `font-weight: bold;` to it.

```html
    <p>
        Get ready for some <strong>bold text</strong>.
    </p>
```

## underline

Like the `strong` tag, use the `u` tag to underline text

*Use with caution; underlined text often denotes a link*

```html
    <p>
        Here comes some <u>underlines</u>.
    </p>
```

## italic

Use the `<em>` tag to make wrapped text italic.

```html
    <p>
        Now for some <em>italics</em>.
    </p>
```

## strikethrough

This effect is added using the `<s>` tag.

```html
    <p>
        This is <s>strikethrough</s>.
    </p>
```
