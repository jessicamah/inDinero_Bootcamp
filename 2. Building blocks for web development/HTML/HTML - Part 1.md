### Getting Started
HTML files are nothing more than simple text files, so to start writing in HTML, you need nothing more than a simple text editor.
If you are using Windows you can use Notepad, which is usually found in the start menu under Programs in Accessories. In this lesson, we are going to use sublime.

### WHat is HTML?
HTML is an abbrevaition of "HyperText Mark-up Langauage". It is the mother tongue of your browser.
Basically it is a language, which makes it possible to present information (e.g. scientific research) on the Internet. What you see when you view a page on the Internet is your browser's interpretation of HTML. It is used to make websites
 
### Tags, Attributes, and Elements
**Tags** is the basic structure of an HTML document, which surround content and apply meaning to it.
 
 Change your document so that it looks like this:
 ```html
 <!DOCTYPE html>
 <html>
 <body>
   This is my first web page
 </body>
 </html>
 ```
The first line on the top, *<!DOCTYPE html>*, is a **document type declaration** and it lets the browser know which flavor of HTML you're using (HTML5, in this case). It's very important to stick this in - If you don't, browsers will assume you don't really know what you're doing and act in a very perculiar way.
 
`<html>` is the opening tag that kicks things off and tells the browser that everything between that and the `</html>` closing tag is an HTML document.

`<body>` and `</body>` is the main content of the document that will appear in the browser window.

**Closing Tags**
The `</body>` and `</html>` put a close to their respective elements.

**Attributes** appears inside the opening tag and their values sit inside a quotation marks. They look something like `<tag attribute="value">Label</tag>`.

**Elements** gives structure to HTML document and tells the browser how you want your website to be presented. Generally elements consists of a start tag, some content, and an end tag.

Example:
`<em>Emphasised text. "em" is short for emphasis</em>`

### Page Titles
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  This is my first web page
</body>
</html>
```
"My first web page" will appear on a tab or the title bar of the window.
The text that you put in between the title tags has become the title of the document.

### Paragraphs
Now that you have the basic structure of HTML documnt, you can mess around with the content a bit.
`<p>` tag is used for paragraphs.

Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  <p>This is my first web page</p>
  <p>I am excited.</p>
</body>
</html>
```
The two lines will now appear on two lines because the browser recognizes them as separate paragraphs.

Think of the HTML content as if it were a book - with paragraphs where appropriate.

### Emphasis
You can emphasize text in a paragraph using `<em>` (empahsis) and `<strong>` (strong importance).

Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  <p>Yes, that really <em> is </em> exciting. <strong>Warning:</strong> level of excitement may cause head to explode.</p>
</body>
</html>
```
Note: Traditionally, browsers will display `<em>` in *italics* and `<strong>` in **bold** by default but they are not the same as `<i>` and `<b>` tags.

### Line breaks
The line breaks tag can also be used to separate lines.

Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  This is my first web page<br>
  I am excited.
</body>
</html>
```
There's no content involved in breaking lines so there is no closing tag.

### Headings

Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  <h1> This is my first web page</h1>
  
  <h2> What is this? </h2>
  <p> A simple page put together using HTML.</p>
</body>
</html>
```

Note that the h1 tag is only used once, as the main heading of the page. h2 to h6, however, can be used as often as desired, but they should always be used in order, as they were intended. For example, an h4 should be a sub-heading of an h3, which should be a sub-heading of an h2.

### Lists
There are three types of list; unordered list, ordered lists and definition lists.

#### Unordered List and Ordered List
Unordered lists and ordered lists work the same way, except that the former is used for non-sequential lists with list items usually preceded by bullets and the latter is for sequential lists, which are normally represented by incremental numbers.

The `<ul>` tag is used to define **unordered lists** and the `<ol>` tag is used to define **ordered lists**. Inside the lists, the `<li>` tag is used to define each list item.

Unordered List Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  <h1>My first web page</h1>

  <h2>What this is</h2>
  <p>A simple page put together using HTML</p>

  <ul>
    <li>To learn HTML</li>
    <li>To show off</li>
    <li>Because I've fallen in love with my computer and want to give her some HTML loving.</li>
  </ul>
</body>
</html>
```

Ordered List Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  <h1>My first web page</h1>

  <h2>What this is</h2>
  <p>A simple page put together using HTML</p>

  <ol>
    <li>To learn HTML</li>
    <li>To show off</li>
    <li>Because I've fallen in love with my computer and want to give her some HTML loving.</li>
  </ol>
</body>
</html>
```
#### Definition Lists
List of terms and decsriptions (such as glosarry), a definition list is your go-to-element

There doesn’t have to be one `<dt>` followed by one `<dd>`, there can be any number of either. For example, if there are a number of words that have the same meaning, there might be a number of dt’s followed by one dd. If you have one word that means various different things, there might be one dt followed by several dd’s.

Definition List Example:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
</head>
<body>
  <h1>Some random glossary thing</h1>
  <dl>
    <dt>HTML</dt>
    <dd>Abbreviation for HyperText Markup Language - a language used to make web pages.</dd>

    <dt>Dog</dt>
    <dd>Any carnivorous animal belonging to the family Canidae.</dd>
    <dd>The domesticated sub-species of the family Canidae, Canis lupus familiaris.</dd>

    <dt>Moo juice</dt>
    <dt>Cat beer</dt>
    <dt>Milk</dt>
    <dd>A white liquid produced by cows and used for human consumption.</dd>
</dl>
</body>
</html>
```

### Links
An **anchor tag** `<a>` is used to define a link, but you also need to add something to the anchor tag - the **destination** of the link 

Syntax:
``` html
<a href="destination">Text<a>
```
The destination of the link is defined in the href attribute of the tag.

A link can also send a user to another part of the same page they are on. You can add an `<id>` attribute to just about any tag, for example
```html
<h2 id="example">Example</h2> <!-- and then link to it by using something like this: -->
<a href="#example">Go to example</a>. <!-- Selecting this link will scroll the page straight to the element with that ID. -->
```

### Images
The `<img>` tags is used to put an image in an HTML document.

Syntax:
```html
<img src="yoursoucehere" width="120" height="90" alt="Logo">
```
The *src attribute* tells the browser where to find the image.

The *width and height attributes* are necessary because if they are excluded, the browser will tend to calculate the size as the image loads, instead of when the page loads, which means that the layout of the document may jump around while the page is loading.

The *alt attribute* is the alternative description. This is an accessibility consideration, providing meaningful information for users who are unable to see the image (if they are visually impaired, for example).

*Note that, like the br tag, because the img element does not enclose any content, no closing tag is required.*

### Tables
The correct use for tables is to do exactly what you would expect a table to do - to structure tabular data.

Syntax:
```html
<table>
  <tr>
    <td> Row 1 Cell 1</td>
    <td> Row 1 Cell 2</td>
    <td> Row 1 Cell 3</td>
  </tr>
  <tr>
    <td> Row 2 Cell 1</td>
    <td> Row 2 Cell 2</td>
    <td> Row 2 Cell 3</td>
  </tr>
</table>
```

The `<table>` elememt defines the table.

The `<tr>` element defines the table row.

The `<td>` element defines the data cell. These must be eclosed in `<tr>` tags, as shown above.

### Forms
Forms are used to collect data inputted by a user. They can be used as interface for a web application, for example, or to send data across the web.

Basic tags used in the actual HTML forms are **form, input, textarea, select and option**.

#### form
It defines the form and within this tag, if you are using a form for a user to submit information (which we are assuming at this level), an **action** attribute is needed to tell the form where its contents will be sent to.

The **method** attribute tells the form how the data in it is going to be send and it can have the value *get*(, which is default, and latches the form information onto a web address, or *post*, which (essentially) invisible sends the form's information.

Note that *get* is used for shorter chunks of non-sensitive information - for example, you might see the information you have submitted in a web site’s search to appear in the web address of its search results page. *post* is used for lengthier, more secure submissions, such as in contact forms.

Syntax:
```html
<form  action="processingsript.html" method="post">
</form>
```

#### input
Input tag is the daddy of all form world.

* `<input type="text">` or simply `<input>` is a standard textbox. This can also have a value attribute, which sets the initial text in the textbox.
* `<input type="password">` is similar to the textbox, but the characters typed in by the user will be hidden.
* `<input type="checkbox">` is a checkbox, which can be toggled on and off by the user. This can also have a checked attribute (<input type="checkbox" checked> - the attribute doesn't require a value), and makes the initial state of the check box to be switched on, as it were.
* `<input type="radio">` is similar to a checkbox, but the user can only select one radio button in a group. This can also have a checked attribute.
* `<input type="submit">` is a button that when selected will submit the form. You can control the text that appears on the submit button with the value attribute, for example <input type="submit" value="Ooo. Look. Text on a button. Wow">.

#### textarea
Textarea is, basically, a large, multi-line textbox.

`<textarea rows="5" cols="20">A big load of text</textarea>`

#### select
The *select* tag works with the *option* tag drop-down select boxes.

```
<select>
    <option>Option 1</option>
    <option>Option 2</option>
    <option value="third option">Option 3</option>
</select>
```

#### Names
All of the tags mentioned above will look very nice presented on the pages but if you hook up your form-handling script, they will all be ignored. This is because the form fields need names. So to all of the fields, the attribute name needs to be added, for example `<input type="text" name="number">`.

```
<form action="processingsript.html" method="post">
  <p>Name:</p>
  <p><input type="text" name="name" value="Your name"></p>

  <p>Comments: </p>
  <p><textarea name="comments" rows="5" cols="20">Your comments</textarea></p>

  <p>Are you:</p>
  <p><input type="radio" name="areyou" value="male"> Male</p>
  <p><input type="radio" name="areyou" value="female"> Female</p>

  <p>Country:</p>
  <p><select>
   <option>Canada</option>
   <option selected>US</option>
   <option>Japan</option>
  </select></p>
  <p><input type="submit"></p>
</form>
```
### HTML Tag:input
A form element that can be represented as a text box, password text box, check box, radio button, submit button, reset button, hidden input field, image (which acts as a submit button), file selection box or general button.

#### Optional Attributes
* `name` can be used so that the value of the element can be processed.
* `type` can be used to specify the type of input. Values can be text (default), password, checkbox, radio, submit, reset, hidden, image, file or button.
* `value` can be used to specify the initial value. It is required when type is set to checkbox or radio. It should not be used when type is set to *file*.
* `checked` can be used when type is set to checkbox or radio to set the initial state of a checkbox or radio button to be selected. It must be used in the format `checked = "checked"`.
* `maxlength` can be used to specify the maximum number of characters allowed in a text box.
* `src` can be used when type is set to image to specify the location of an image file.
* `alt` can be used when type is set to image to specify the alternative text of the image, whoch should be a short of description.
* `accept` can be used when type is set to file to specify which file-types should be accepted. This is a comma-separated list of MIME types.
* `disabled` can be used to disable an element. It must be used in format `disabled="disabled"`.
* `readonly` can be used to specify that the value of the element can not be changed. It must be used in the format `readonly="readonly"`.
* `accesskey` can be used to associate a keyboard shortcut to the element.
* `tabindex` can be used to specify where the element appears in the tab order of the page.

### Comment in HTML
`<!-- This is a comment -->`

### The following code incorporates all of the methods that have been explained
```html
<!DOCTYPE html>
<html>
<head>
  <title>My first web page</title>
  <!-- This is a comment, by the way -->
</head>
<body>
  <h1>My first web page</h1>

  <h2>What this is</h2>
  <p>A simple page put together using HTML. <em>I said a simple page put together using HTML.</em> A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML. A simple page put together using HTML.</p>

  <h2>Why this is</h2>
  <ul>
  <li>To learn HTML</li>
  <li>
   To show off
   <ol>
     <li>To my boss</li>
     <li>To my friends</li>
     <li>To my cat</li>
     <li>To the little talking duck in my brain</li>
   </ol>
  </li>
  <li>Because I have fallen in love with my computer and want to give her some HTML loving.</li>
  </ul>

  <h2>Where to find the tutorial</h2>
  <p><a href="http://www.htmldog.com"><img src="http://www.htmldog.com/badge1.gif" width="120" height="90" alt="HTML Dog"></a></p>

  <h3>Some random table</h3>
  <table>
  <tr>
    <td> Row 1 Cell 1</td>
    <td> Row 1 Cell 2</td>
    <td> Row 1 Cell 3</td>
  </tr>
  <tr>
    <td> Row 2 Cell 1</td>
    <td> Row 2 Cell 2</td>
    <td> Row 2 Cell 3</td>
  </tr>
  </table>

  <h3>Some random form</h3>
  <p><strong>Note:</strong> It looks the part, but won't do a damned thing.</p>

  <form action="somescript.html" method="post">

  <p>Name:</p>
  <p><input name="name" value="Your name"></p>

  <p>Comments: </p>
  <p><textarea rows="10" cols="20" name="comments">Your comments</textarea></p>

  <p>Are you:</p>
  <p><input type="radio" name="areyou" value="male"> Male</p>
  <p><input type="radio" name="areyou" value="female"> Female</p>

  <p>Country:</p>
  <p><select>
  <option>Canada</option>
  <option selected>US</option>
  <option>Japan</option>
  </select></p>
  <p><input type="submit"></p>
  </form>
</body>
</html>
```
