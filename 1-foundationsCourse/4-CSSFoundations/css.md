[TOC]
# 1 Intro to CSS
## 1.1 Selectors
- Universal Selector
  ```css
  * {
    color: purple;
  }
  ```
- Type Selectors
  A type selector (or element selector) will select all elements of the given element type, and the syntax is just the name of the element:
  ```html
  <div>Hello world!</div>
  <div>hello again</div>
  <p>hi</p>
  <div>okay, bye</div>
  ```
  ```css
  div {
    color: white;
  }
  ```
- Class Selectors
  Class selectors will select all elements with the given class, which is just an attribute you place on an HTML element.
  ```html
  <!-- index.html -->

  <div class="alert-text">Please agree to our terms of service.</div>
  ```

  ```css
  .alert-text {
    color: red;
  }
  ```
  Classes aren’t required to be specific to a particular element, so you can use the same class on as many elements as you want.
  Another thing you can do with the class attribute is to add multiple classes to a single element as a space-separated list, such as ```class="alert-text severe-alert"```
- ID selectors
  ```html
  <!-- index.html -->

  <div id="title">My Awesome 90's Page</div>
  ```
  ```css
  /* styles.css */

  #title {
    background-color: red;
  }
  ```
  The major difference between classes and IDs is that an element can only have one ID. 
  An ID cannot be repeated on a single page, and the ID attribute should not contain any whitespace at all.
- The grouping selector
  ```css
  .read {
    color: white;
    background-color: black;
    /* several unique declarations */
  }

  .unread {
    color: white;
    background-color: black;
    /* several unique declarations */
  }
  ```
  ```css
  .read,
  .unread {
    color: white;
    background-color: black;
  }

  .read {
    /* several unique declarations */
  }

  .unread {
    /* several unique declarations */
  }
  ```

- Chaining selectors
  ```css
  .subsection.header {
    color: red;
  }

  .subsection#preview {
    color: blue;
  }
  ```
- Descendant Combinator
  ```html
  <!-- index.html -->

  <div class="ancestor">
    <!-- A -->
    <div class="contents">
    <!-- B -->
      <div class="contents"><!-- C --></div>
    </div>
  </div>

  <div class="contents"></div>
  <!-- D -->
  ```

  ```css
  .ancestor .contents {
    /* some declarations */
  }
  ```

##1.2 Properties to get started with
```css
p {
  /* hex example: */
  color: #1100ff;
}

p {
  /* rgb example: */
  color: rgb(100, 0, 127);
}

p {
  /* hsl example: */
  color: hsl(15, 82%, 56%);
}
```

[CSS color values](https://www.w3schools.com/cssref/css_colors_legal.php)

```font-family```
[Best web safe fonts of HTML and CSS](https://www.w3schools.com/cssref/css_websafe_fonts.php)

```font-size```
```font-weight```

```text-align```

```css
img {
  height: auto;
  width: 500px;
}
```

##1.3 Adding CSS to HTML
- external CSS
  ```css
  <head>
    <link rel="stylesheet" href="styles.css" />
  </head>
  ```
- internal CSS
  ```css
  <head>
    <style>
      div {
        color: white;
        background-color: black;
      }

      p {
        color: red;
      }
    </style>
  </head>

  <body>
  ...
  </body>
  ```
- inline Css
  ```css
  <body>
    <div style="color: white; background-color: black;">hhhh</div>
  </body>
  ```

# 2 The Cascade

The cascade is what determines which rules actually get applied to our HTML.
- [specificity](https://www.w3schools.com/Css/css_specificity.asp)
  inline styles > id selectors > class selectors > type selectors > universal selector(*) = combinators(+, ~, >, empty space)
- inheritance
  Typography based properties (`color`, `font-size`, `font-family`, etc.) are usually inherited, while most other properties aren’t.
  The exception to this is when directly targeting an element, as this always beats inheritance
- rule order
  Whichever rule was the last defined is the winner.

Every CSS selector has its place in the specificity hierarchy.

There are four categories which define the specificity level of a selector:

1. Inline styles - Example: ```<h1 style="color: pink;">```
2. IDs - Example: #navbar
3. Classes, pseudo-classes, attribute selectors - Example: .test, :hover, [href]
4. Elements and pseudo-elements - Example: h1, ::before

Start at 0, add 100 for each ID value, add 10 for each class value (or pseudo-class or attribute selector), add 1 for each element selector or pseudo-element.
# 3 Inspecting HTML and CSS
Element: Ctrl + Shift + C	
Console: Ctrl + Shift + J	
Your last panel: F12 / Ctrl + Shift + I

C stands for CSS.
J for JavaScript.
I designates your choice.

windows: ```start chrome --auto-open-devtools-for-tabs```
linus: ```google-chrome --auto-open-devtools-for-tabs```


https://developer.chrome.com/docs/devtools/css/
https://developer.chrome.com/docs/devtools/dom/#scroll2

[Shortcuts](https://developer.chrome.com/docs/devtools/shortcuts/#elements)

# 4 The box model

## 4.1 border, margin and padding


![border, margin, padding](https://cdn.statically.io/gh/TheOdinProject/curriculum/main/foundations/html_css/css-foundations/the-box-model/imgs/box-model.png)

[border property](https://developer.mozilla.org/en-US/docs/Web/CSS/border)
[padding property](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)

## 4.2 the alternative CSS box model
The content area width is that width minus the width for the padding and border (see image below).
```css
.box {
  box-sizing: border-box;
}
```
To use the alternative box model for all of your elements (which is a common choice among developers), set the `box-sizing` property on the `<html>` element and set all other elements to inherit that value:
```css
html {
  box-sizing: border-box;
}
*,
*::before,
*::after {
  box-sizing: inherit;
}
```

[margin tutorial](https://css-tricks.com/almanac/properties/m/margin/)

[the box model (important)](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/The_box_model)



## 4.3 outer display type
If a box has an outer display type of `block`, then:

- The box will break onto a new line.
- The width and height properties are respected.
- Padding, margin and border will cause other elements to be pushed away from the box.
- If width is not specified, the box will extend in the inline direction to fill the space available in its container. In most cases, the box will become as wide as its container, filling up 100% of the space available.
Some HTML elements, such as `<h1> and <p>`, use block as their outer display type by default.

If a box has an outer display type of `inline`, then:

- The box will not break onto a new line.
- The width and height properties will not apply.
- Top and bottom padding, margins, and borders will apply but will not cause other inline boxes to move away from the box.
- Left and right padding, margins, and borders will apply and will cause other inline boxes to move away from the box.
Some HTML elements, such as `<a>, <span>, <em> and <strong> `use inline as their outer display type by default. 



## 4.3 inner display type

You can change the inner display type for example by setting `display: flex;`. The element will still use the outer display type `block` but this changes the inner display type to `flex`.

An element with `display: inline-block` does a subset of the block things we already know about:
- The width and height properties are respected.
padding, margin, and 
- border will cause other elements to be pushed away from the box.

Where this can be useful is when you want to give a link a larger hit area by adding padding. `<a> `is an inline element like `<span>`; you can use `display: inline-block` to allow padding to be set on it, making it easier for a user to click the link.


# 5 Block and Inline

[normal flow](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow)
[w3 school block and inline elements](https://www.w3schools.com/html/html_blocks.asp)
[difference examples](https://www.digitalocean.com/community/tutorials/css-display-inline-vs-inline-block)


