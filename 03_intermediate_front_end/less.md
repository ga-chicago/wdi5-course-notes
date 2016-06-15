# LESS

[LESS](http://lesscss.com) is a superset of CSS and a CSS transpiler. It takes a special CSS syntax and turns it into regular CSS.

## Installation and usage

Run `npm install -g less` to install the LESS transpiler.

## LESS Features

### Variables

You can use variables to hold a value and reuse it in other parts of the file.

```less
@heading-color: #505050;
@body-color: #272727;

h1, h2, h3, h4, h5, h6 {
  color: @heading-color;
}

p {
  color: @body-color;
}
```

### Nesting

You can nest selectors within other selectors. This makes writing CSS faster and more efficient.

With HTML like this:

```html
<ul>
  <li>My</li>
  <li>list</li>
</ul>
```

```less
ul {
  background: #505050;
  list-style: none;

  li {
    color: #f7f7f7;
    display: inline;
  }
}
```

### Mixins

A mixin is sort of like a function. It can take arguments and whatever the contents of the mixin are, they will be transferred into the CSS selector that you add it to.

```less
// Creates a mixin that changes background colors
background-mixin(@color) {
  background-color: @color;
}

// Now we can use this mixin in any other class definition
.my-element {
  .background-mixin(blue);
}
```

The above would turn into this CSS:

```css
.my-element {
  background-color: blue;
}
```

### Imports

You can import files and turn multiple LESS files into a single one. This is useful for modularizing your LESS. A common practice is to have a `style.less` file which imports all the style rules from external LESS files.

```less
@import 'variables';
@import 'colors';
@import 'typography';
@import 'grid';
```
