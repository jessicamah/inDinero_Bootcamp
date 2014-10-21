#### HTML Part 2

### Span and Div
The difference between `span` and `div` is that a span element is **in-line** and usually used for a small chunk of HTML
inside a line (such as inside a paragraph) whereas a div (division) element is **block-line** (which is basically equivalent
to having a line-break before and after it) and used to group larger chunks of code.

```html
<div id="scissors">
  <p> This is <span class="paper">crazy</span></p>
</div>
```

`div` and especially `<span>` shouldn't actually be used that often. Whenever there is a sensible alternative that should be used instead.
For example, if you want to emphasize the word "crazy" and the class "paper" is adding italics for visual emphasis,
then, for richer, more meaningful content, the code might look like this:

```html
<div id="scissors">
  <p>This is <em class="paper">crazy</em></p>
</div>
```

### Meta Tags
Meta tags don't do anything to the content that is presented in the browser window, but they are used by the likes of search
engines to catalogue information about the web page.

There is one meta tag which can be used as many times as you desire inside a head element and they can contain the attributes charset, name, http-equiv, and content.

When the name or http-equiv attribute is used, the content attribute is then used in conjunction with them to apply meta data itself.

#### Names
The name attribute can be anything you like. The most commonly used names are author, description, and keywords. author is used to explicitly state one of the HTML page’s authors and description is often used by search engines (such as Google) to display a description of a web page in its search results.

#### HTTP Equivalents
The http-equiv attribute can be used instead of the name attribute and will make an HTTP header, which is information sent to the server where the web page is held. The attribute should rarely be used (although see charset note, below) but the value can be:

* `content-type`, an encoding declaration, defining what character set is being used,
* `default-style`, the preferred stylesheet from a selection of link or style elements,
* `refresh`, which defines how often (in seconds) a page automatically refreshes or if it should automatically redirect to another page. Not great for accessibility.

The charset attribute can be used as a shorthand method to define an HTML document’s character set, which is always a good thing to do.
`<meta charset="utf-8">` is the same as `<meta http-equiv="content-type" content="text/html; charset=utf-8">`.

### Tables: rowspan and colspan
```html
<table>
  <tr>
    <th>Column 1 heading</th>
    <th>Column 2 heading</th>
    <th>Column 3 heading</th>
  </tr>
  <tr>
    <td>Row 2, cell 1</td>
    <td colspan="2">Row 2, cell 2, also spanning Row 2, cell 3</td>
  </tr>
  <tr>
    <td rowspan="2">Row 3, cell 1, also spanning Row 4, cell 1</td>
    <td>Row 3, cell 2</td>
    <td>Row 3, cell 3</td>
  </tr>
  <tr>
    <td>Row 4, cell 2</td>
    <td>Row 4, cell 3</td>
  </tr>
</table>
```
The `colspan` attribute, which means "column span" will span the cell over the number of cells that is specified. This means, in this example, that there is no need for a third td element - two cells are merged into one.

The `rowspan` attribute is similar to colspan, except, obviously, it will span across rows rather than columns. Again, the cells that it spans should be removed. In this example, because it spans over the fourth row, there are only two cells in that row.

### Header cells

The first difference is that the td tags of the first row have been replaced with th tags. Whereas a td is a standard data cell, th is a header cell. As with td elements, these must be enclosed inside tr elements.

### Sectioning
Sectioning involves a handful of tags that can be used to define specific parts of a page, usch as articles, headers, footers, and navigation.

#### Articles and Sections
An `article` element can be used to mark up a **standalone section** of content. This could be used just once, if you think of a blog post as an article, for example, or a number of times, if you imagine replicating a traditional newspaper page with numerous articles.

A `section` element represents a more **general section** and could be used to split up an article, or to represent chapters, for example.

```html
<article>
  <section id="intro">
    <p>[An introduction]</p>
  </section>
  <section id="main_content">
    <p>[Content]</p>
  </section>
  <section id="related">
    <ul>
      <li><a href="that.html">That related article</a></li>
      <li><a href="this.html">This related article</a></li>
    </ul>
  </section>
</article>
```

#### Headers and Footers
`header` and `footer` provide further specialized, self-descriptuve, sections:
```html
<body>
<article>
  <header>
    <h1>Alternatively&hellip;</h1>
    <p>[An introduction]</p>
  </header>
  <section id="main_content">
    <p>[Content]</p>
  </section>
  <footer>
    <p>[End notes]</p>
  </footer>
</article>
<footer>
  <p>[Copyright bumf]</p>
</footer>
</body>
```
The footer is the footer of the section in which it is contained. So, in the above example, the first footer is the footer of the article and the second footer is the footer of the page.

#### Asides
An aside can be used to represent content that is related the content surrounding it. Think of pull-quotes or snippets of related information in an article:
```html
<section id="main_content">
  <h1>Tixall</h1>
  <p>[All about Tixall]</p>
  <aside>
    <h2>Tixall Obelisk</h2>
    <p>[A short note about Tixall Obelisk]</p>
  </aside>
  <p>[Maybe a bit more about Tixall]</p>
</section>
```

#### Navigation
Finally, there’s nav, used to mark up a group of navigation links:
```
<nav id="main_nav">
  <ul>
    <li><a href="/tutorials/">Tutorials</a></li>
    <li><a href="/reference/">Reference</a></li>
    <li><a href="/articles/">Articles</a></li>
    <li><a href="/about/">About us</a></li>
  </ul>
</nav>
```
