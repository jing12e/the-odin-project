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
```

```font-family```
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


  
