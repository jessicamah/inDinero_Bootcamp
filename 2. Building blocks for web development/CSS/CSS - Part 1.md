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


### Colors
CSS brings 16,77,215 colors to your disposal. They can take the form of a name, and RGB (red/green/blue) value or hex code.

For example
```css
color: red;
color: rgb(255,0,0);
color: rgb(100%,0%,0%)
color: #ff0000
color: #f00
```

The three values in the RGB value are from 0 to 255, 0 being the lowest level (no red, for example), 255 being the highest level (full red, for example). These values can also be a percentage

Hexadecimal (previously and more accurately known as "sexadecimal") is a base-16 number system. We are generally used to the decimal number system (base-10, from 0 to 9), but hexadecimal has 16 digits, from 0 to f.

The hex number is prefixed with a hash character (#) and can be three or six digits in length. Basically, the three-digit version is a compressed version of the six-digit (#ff0000 becomes #f00, #cc9966 becomes #c96, etc.). The three-digit version is easier to decipher (the first digit, like the first value in RGB, is red, the second green and the third blue) but the six-digit version gives you more control over the exact color.

#### color and background-color
Colors can be applied by using color and background-color (note that this must be the American English "color" and not "colour").

A blue background and yellow text could look like this:
```css
h1 {
  color: yellow;
  background-color: blue;
}
```

These colors might be a little too harsh, so you could change the code of your CSS file for slightly different shades:
```css
body {
  font-size: 14px;
  color: navy;
}

h1 {
  color: #ffc;
  background-color: #009;
}
```

### Text
* **font-family** is the font itself, such as Times New Roman, Arial, or Verdana.
* **font-size** is the size of the font.
* **font-weight** is the states whether the text is bold or not. Most commonly this is used as font-weight: bold or font-weight: normal but other values are bolder, lighter, 100, 200, 300, 400 (same as normal), 500, 600, 700 (same as bold), 800 or 900.
* **font-style** is the states whether the text is italic or not. It can be *font-style: italic* or *font-style: normal*.
* **text-decoration** is the states whether the text has got a line running under, over, or through it.
```css
text-decoration: underline /* does what you would expect. */
text-decoration: overline /* places a line above the text. */
text-decoration: line-through /* puts a line through the text ("strike-through"). */
```
This property is usually used to decorate links and you can specify no underline with `text-decoration: none`.

* **text-transform** will change the case of the text
```css
text-transform: capitalize /* turns the first letter of every word into uppercase. */
text-transform: uppercase /* turns everything into uppercase. */
text-transform: lowercase /* turns everything into lowercase. */
text-transform: none /* I’ll leave for you to work out. */
```

So, a few of these things used together might look like this:
```css
body {
  font-family: arial, helvetica, sans-serif;
  font-size: 14px;
}

h1 {
  font-size: 2em;
}

h2 {
  font-size: 1.5em;
}

a {
  text-decoration: none;
}

strong {
  font-style: italic;
  text-transform: uppercase;
}
```

* **Text spacing**
The `letter-spacing` and `word-spacing` properties are for spacing between letters or words. The value can be a length or normal.

The `line-height` property sets the height of the lines in an element, such as a paragraph, without adjusting the size of the font. It can be a number (which specifies a multiple of the font size, so "2" will be two times the font size, for example), a length, a percentage, or normal.

The `text-align` property will align the text inside an element to left, right, center, or justify.

The `text-indent` property will indent the first line of a paragraph, for example, to a given length or percentage. This is a style traditionally used in print, but rarely in digital media such as the web.
```css
p {
  letter-spacing: 0.5em;
  word-spacing: 2em;
  line-height: 1.5;
  text-align: center;
}
```

### Margins and Padding
margin and padding are the two most commonly used properties for spacing-out elements. A margin is the space outside something, whereas padding is the space inside something.

```css
h2 {
  background-color: #ccc;
  font-size: 1.5em;
  margin: 20px;
  padding: 40px;
}
```
The four sides of an element can also be set individually. `margin-top`, `margin-right`, `margin-bottom`, `margin-left`, `padding-top`, `padding-right`, `padding-bottom` and `padding-left` are the self-explanatory properties you can use.

### The Box Model
Margins, padding and borders are all part of what’s known as the Box Model. The Box Model works like this: in the middle you have the content area (let’s say an image), surrounding that you have the padding, surrounding that you have the border and surrounding that you have the margin.

```html
__________________________________________
| Margin box                             |
|  ____________________________________  |
|  |  border box                      |  |
|  |  ______________________________  |  |
|  |  |   padding box              |  |  |
|  |  |   ______________________   |  |  |
|  |  |  |     element box     |   |  |  |
|  |  |  |_____________________|   |  |  |
|  |  |                            |  |  |
|  |  |____________________________|  |  |
|  |                                  |  |
|  |__________________________________|  |
|                                        |
|________________________________________|
```

### Borders
Borders can be applied to most HTML elements within the body.

To make a border around an element, all you need is `border-style`. The values can be **solid**, **dotted**, **dashed**, **double**, **groove**, **ridge**, **inset** and **outset**.

`border-width` sets the width of the border, most commonly using pixels as a value. There are also properties for `border-top-width`, `border-right-width`, `border-bottom-width` and `border-left-width`.

`border-color` sets the color.

```css
h2 {
  border-style: dashed;
  border-width: 3px;
  border-left-width: 10px;
  border-right-width: 10px;
  border-color: red;
}
```

### The following incorporates everything:
```css
body {
  font-family: arial, helvetica, sans-serif;
  font-size: 14px;
  color: black;
  background-color: #ffc;
  margin: 20px;
  padding: 0;
}

/* This is a comment, by the way */

p {
  line-height: 21px;
}

h1 {
  color: #ffc;
  background-color: #900;
  font-size: 2em;
  margin: 0;
  margin-bottom: 7px;
  padding: 4px;
  font-style: italic;
  text-align: center;
  letter-spacing: 0.5em;
  border-bottom-style: solid;
  border-bottom-width: 0.5em;
  border-bottom-color: #c00;
}

h2 {
  color: white;
  background-color: #090;
  font-size: 1.5em;
  margin: 0;
  padding: 2px;
  padding-left: 14px;
}

h3 {
  color: #999;
  font-size: 1.25em;
}

img {
  border-style: dashed;
  border-width: 2px;
  border-color: #ccc;
}

a {
  text-decoration: none;
}

strong {
  font-style: italic;
  text-transform: uppercase;
}

li {
  color: #900;
  font-style: italic;
}

table {
  background-color: #ccc;
}
```