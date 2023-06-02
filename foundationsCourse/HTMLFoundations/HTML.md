1 Introduction To HTML And CSS
===
- HTML (HyperText Markup Language) puts information on a webpage.
- CSS positions that information, gives it color, changes the font, and makes it look great!
- They are only concerned with presenting information

[Article](https://www.freecodecamp.org/news/html-css-and-javascript-explained-for-beginners/)
[HTML vs. CSS vs. Javascript](https://brytdesigns.com/html-css-javascript-whats-the-difference)

- The main reason why it’s important to know **HTML** is because it allows you as a website owner to create the basic structure of you website,

- **CSS** is a static programming language

- **JavaScript** allows you to change CSS and HTML elements on your website after the site has been loaded, which gives you the ability to make your site more interactive and engaging for users with animations, embedded video media, and more.

![picture](https://admin.brytdesigns.com/wp-content/uploads/2019/12/html_css_javascript_infographic.png)

Some of the most common web development languages include HTML, CSS, JavaScript, PHP, Python, Ruby, and SQL.

- **Ruby** is a scalable and fast programming language

- **WordPress** is built mainly with powerful PHP code even though HTML and CSS are used as well.
  

**Addtional resources**
[FreeCodeCamp](https://www.freecodecamp.org/learn)
[DevDocs.io](https://devdocs.io/)

2 Elements And Tags
===
forward slash `/`

A full paragraph element looks like this:
```html
<p> some text content</p>
```
self-closing tags or empty elements: elements that do not have a closing tag
```html
<br /> or <img/>
<br> or <img>
```

3 HTML Boilerplate
===
- The DOCTYPE
  ```<!DOCTYPE html>```
- HTML Element
  ```html
  <html lang="en">
  </html>
  ```
- Head Element
  
- The Charset Meta Element
We should always have the meta tag for the charset encoding of the webpage in the head element: 
    ```html
    <meta charset="utf-8">
    ```


- Title Element
Another element we should always include in the head of an HTML document is the title element:
    ```html
    title>My First Webpage</title>
    ```
- Body Element
  This is where all the content that will be displayed to users will go - the text, images, lists, links, and so on.
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>My First Webpage</title>
        </head>

        <body>
        </body>
    </html>
    ```
- View HTML Files in the Browser
  
4 Working With Text
===
- Create paragraph
  A paragraph element is defined by wrapping text content with a `<p>` tag.
- Headings
  `<h1> - <h6>`
- Strong Element
  bold `<strong>`
- Em Element
  italic `<em>`
- Nesting and Indentation
  use indentation to make the level of nesting clear and readable
  parent, child, and sibling relationships between elements
- HTML Comments
  ```html
  <!-- I am a html comment -->
  ```