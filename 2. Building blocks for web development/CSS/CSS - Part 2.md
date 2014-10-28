#### CSS Part 2

### Class and ID Selectors
* **Class** can be used to identify more than one.
* **ID** can be used to identify one element.

In the CSS, a class selector is a name preceded by a full stop (".") and an ID selector is a name preceded by a hash character ("#").
```css
#top {
  background-color: #ccc;
  padding: 20px
}

.intro {
  color: red;
  font-weight: bold;
}
```

The HTML refers to the CSS by using the attributes id and class. It could look something like this:
```html
<div id="top">
  <h1>Chocolate curry</h1>
  <p class="intro">This is my recipe for making curry purely with chocolate</p>
  <p class="intro">Mmm mm mmmmm</p>
</div>
```

### Grouping and Nesting
Two ways that you can simplify your code - both HTML and CSS - and make it easier to manage.

**Grouping**
You can give the same properties to a number of selectors without having to repeat them.

```css
h2 {
  color: red;
}

.thisOtherClass {
  color: red;
}

.yetAnotherClass {
  color: red;
}

/* you can make it like this */
h2, .thisOtherClass, .yetAnotherClass {
  color: red;
}
```

**Nesting**
If the CSS is structured well, there shouldn’t be a need to use many class or ID selectors. This is because you can specify properties to selectors within other selectors.

```css
#top {
  background-color: #ccc;
  padding: 1em
}

#top h1 {
  color: #ff0;
}

#top p {
  color: red;
  font-weight: bold;
}
```

```html
<div id="top">
  <h1>Chocolate curry</h1>
  <p>This is my recipe for making curry purely with chocolate</p>
  <p>Mmm mm mmmmm</p>
</div>
```

### Pseudo Classes
These are bolts on to the selectors to specify a state or relation to the selector. They take the form of `selector:pseudo_class { property: value; }`, simply with a colon in between the selector and the pseudo class.

### Links
link, targeting unvisited links, and visited, targeting, you guessed it, visited links, are the most basic pseudo classes.
```css
a:link {
  color: blue;
}

a:visited {
  color: purple;
}
```

### Dynamic Pseudo Classes
* **active** is for when something activated by the user, such as when a link is clicked on.
* **hover** is for a when something is passed over by an input from the user, such as when a cursor moves over a link.
* **focus is for when something gains focus, that is when it is selected by, or is ready for, keyboard input.

### First Children
```html
<body>
  <p>I’m the body’s first paragraph child. I rule. Obey me.</p>
  <p>I resent you.</p>
</body>
```

```css
p:first-child {
  font-weight: bold;
  font-size: 40px;
}
```