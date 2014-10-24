### Getting Started
CSS, or Cascading Styles Sheets, is a way to style and present HTML. Whereas the HTML is the meaning or content, the style sheet is the presentation of that document.

Style don't smell or taste anything like HTML, they have a format of **property: value** and most properties can be applied to most HTML tags.

### Applying CSS
There are three ways to apply CSS to HTML: in-line, internal and external.

### In-line
In-line styles are plonked straight into the HTML tags using the `style` attribute.
They look something like this:

```css
<p style="color: red">text</p>
```
This will make that specific paragraph red.
But, if you remember, the best-practice approach is that the HTML should be a stand-alone, presentation free document, and so in-line styles should be avoided wherever possible.

### Internal
Embedded, or internal, styles are used for the whole page. Inside the *head* element, the **style** tags surround all of the styles for the page.

```html
<!DOCTYPE html>
<html>
<head>
<title>CSS Example</title>
<style>
  p {
    color: red;
  }

  a {
    color: blue;
  }

</style>
</head>
<body>
  <p> This is red </p>
  <a href="#"> This tag is blue </a>
</body>
</html>
```
This will make all of the paragraphs in the page red and all of the links blue.
Although preferable to soiling our HTML with inline presentation, it is similarly usually preferable to keep the HTML and the CSS files separate, and so we are left with our savior.

### External
External styles are used for the whole, multiple-page website. There is a separate CSS file, which will simply look something like:

```css
p {
  color: red;
}

a {
  color: blue;
}
```
If this file is saved as **style.css** in the same directory as your HTML page then it can be linked to in the HTML like this:

```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS Example</title>
  <link rel="stylesheet" href="style.css">
...
```

### Selectors, Properties, and Values
For each selector there are **properties** inside curly brackets, which simply take the form of words such as *color*, *font-weight* or *background-color*.

A **value** is given to the property following a **colon** (NOT an "equals" sign) and **semi-colons** separate the properties.

```css
body {
  font-size: 14px;
  color: navy;
}
```

This will apply the given values to the font-size and color properties to the body selector.

### Lengths and Percentages
There are many property-specific units for values used in CSS, but there are some general units that are used by a number of properties and it is worth familiarizing yourself with these before continuing.

* **px** (such as font-size: 12px) is the unit for pixels.
* **em** (such as font-size: 2em) is the unit for the calculated size of a font. So “2em”, for example, is two times the current font size.
* **pt** (such as font-size: 12pt) is the unit for points, for measurements typically in printed media.
* **%** (such as width: 80%) is the unit for… wait for it… percentages.

Other units include `pc` (picas), `cm` (centimeters), `mm` (millimeters) and `in` (inches).

When a value is **zero**, you do not need to state a unit. For example, if you wanted to specify no border, it would be border: 0.
