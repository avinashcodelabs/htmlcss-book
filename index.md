# HTML5 and CSS3: The Essential Guide <!-- omit in toc -->

![react-logo](assets/cover-page.jpg)

---

## Contents <!-- omit in toc -->

- [1. Introduction](#1-introduction)
  - [1.1. An Intro](#11-an-intro)
  - [1.2. How web works?](#12-how-web-works)
  - [1.3. Chrome DevTools](#13-chrome-devtools)
  - [1.4. The Big Picture](#14-the-big-picture)
- [2. Basic Web Pages](#2-basic-web-pages)
  - [2.1. Structure of a web page](#21-structure-of-a-web-page)
  - [2.2. HTML Elements or Tags](#22-html-elements-or-tags)
    - [2.2.1. Page Title `<title>`](#221-page-title-title)
    - [2.2.2. Paragraphs `<p>`](#222-paragraphs-p)
    - [2.2.3. headings `<h>`](#223-headings-h)
    - [2.2.4. Unordered Lists `<ul>`](#224-unordered-lists-ul)
    - [2.2.5. Ordered Lists `<ol>`](#225-ordered-lists-ol)
    - [2.2.6. Emphasis (Italic) Elements](#226-emphasis-italic-elements)

## 1. Introduction

### 1.1. An Intro

- HyperText Markup Language (HTML)
- Cascading Style Sheets (CSS), and
- JavaScript
  
are the languages that run the web.

- **HTML** is for adding meaning to raw content by **marking** it up.
- **CSS** is for formatting that marked up content.
- **JavaScript** is for making that content and formatting interactive.

> Note: JavaScript can be used outside the browser/HTML environment like in Node.js.

### 1.2. How web works?

For example, the URL,  <http://google.com>, how it goes from client/browser to server and back to client.

1. Browser send http request to server
2. Server returns http response to browser
3. The http response contains HTML
4. Browser reads HTML to construct the DOM (Document Object Model).
5. Finally, browser, renders (displays) DOM in the browser.

- **URL** (Uniform Resource Locator)
- **DOM** - an in-memory representation of the elements on the HTML web page. This is what JavaScript interact with.

### 1.3. Chrome DevTools

- F12,
- Network tab,
- HTTP request
- HTTP response
- Preview
- status code
- content type
- Filter network requests

### 1.4. The Big Picture

Think of HTML as the abstract text and images behind a web page, CSS as the page that actually gets displayed, and JavaScript as the behaviors that can manipulate both HTML and CSS.

Ex,

![big-picture](assets/big-picture.png)

- In above example, we mark some particular text as a `paragraph` with this `<p></p>` HTML.
- Then, we set the color of that paragraph with some CSS.
- When the user clicks it on it, we run some JavaScript.

## 2. Basic Web Pages

HTML defines the content of every web page on the Internet. By “marking up” your raw content with HTML tags, you’re able to tell web browsers how you want different parts of your content to be displayed.

### 2.1. Structure of a web page

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Metadata goes here -->
  </head>
  <body>
    <!-- Content goes here -->
  </body>
</html>
```

- The line `<!DOCTYPE html>` tells browsers that this is an HTML5 web page.
- The entire web page needs to be wrapped in `<html>` tags.
- `<html>` text is called an **opening tag** and `</html>` is called a **closing tag**.
- Everything inside of these tags are considered part of the `<html>` **element**, which is what gets created when a web browser parses the HTML tags.

   ![big-picture](assets/html-tag.png)

- Inside of the `<html>` element, we have two more elements called `<head`> and `<body>`.
- A web page’s `head` contains all of its metadata such as page title, CSS, JavaScript, fonts etc which are required to render the page but we don’t necessarily want the user to see them.
- The `<body>` element, which represents the visible content of the page. In our case, its empty since it has an empty `<body>`.

  ![big-picture](assets/head-body.png)

- Anything that starts with `<!--` and ends with `-->` will be completely ignored by the browser and these are called comments.

### 2.2. HTML Elements or Tags

Create a page, `index.html` and lets putting the html elements into it.

#### 2.2.1. Page Title `<title>`

This is the title of webpage denoted ny `<title>` element. The browser displays this in the tab for our page, and search engines such as google, duckduckgo displays it in search results.

Result in the browser,

 ![big-picture](assets/page-title.png)

#### 2.2.2. Paragraphs `<p>`

 The `<p>` element marks all the text inside it as a distinct paragraph.

 ```html
<!DOCTYPE html>
<html>
  <head>
    <title>Welcome to HTML</title>
  </head>
  <body>
    <p>Hello HTML, you are awesome.</p>
  </body>
</html>
 ```

 Result,

 ![big-picture](assets/p.png)

#### 2.2.3. headings `<h>`

- Headings are like titles, but they’re actually displayed on the page.
- HTML provides six levels of headings, `<h1>` `<h2>` `<h3>` `<h4>` `<h5>` and `<h6>`
- Higher the number, lesser the prominence heading.

```html
<body>
  <h1>Welcome homie</h1>
  <p>Hello HTML, you are awesome.</p>
</body>
```

 ![big-picture](assets/h.png)

What of second and other level of headings?
Lets see them,

 ```html
 <body>
  <h1>Welcome homie</h1>
  <h2>Welcome homie</h2>
  <h3>Welcome homie</h3>
  <h4>Welcome homie</h4>
  <h5>Welcome homie</h5>
  <h6>Welcome homie</h6>
  <p>Hello HTML, you are awesome.</p>
</body>
 ```

This should result in a web page that looks something like this:

![big-picture](assets/h1-h6.png)

#### 2.2.4. Unordered Lists `<ul>`

Wrapping content in `<ul>` tags tells a browser that whatever is inside should be rendered as an **unordered list**. To denote individual items in that list, we wrap them in `<li>` tags, such as,

```html
<ul>
  <li>Facebook</li>
  <li>Instagram</li>
  <li>WhatsApp</li>
</ul>
```

In browser,

 ![big-picture](assets/ul.png)

Note: `<ul>` element should only be containing `<li>` as a direct child.

❌ BAD

```html
<ul>
  <p>hello</p>
</ul>
```

✅ GOOD

```html
<ul>
  <li><p>hello</p></li>
</ul>
```

#### 2.2.5. Ordered Lists `<ol>`

With an unordered list, sequence of list items does matter, but when we need the sequence to our list item, thats when reach out to ordered list `<ol>`

To create an ordered list, simply change the parent `<ul>` element to `<ol>`.

```html
<ol>
  <li>Facebook</li>
  <li>Instagram</li>
  <li>WhatsApp</li>
</ol>
```

Would result in,

![big-picture](assets/ol.png)

Notice that the browser automatically incremented the count for each `<li>` element.

#### 2.2.6. Emphasis (Italic) Elements

<!-- ## 3. Links and Images

## 4. Hello, CSS

## 5. The Box Model

## 6. CSS Selectors

## 7. Floats

## 8. Flexbox

## 9. Grid

## 10. Advanced Positioning

## 11. Responsive Design

## 12. Responsive Images

## 13. Semantic HTML

## 14. Forms

## 15. Web Typography -->