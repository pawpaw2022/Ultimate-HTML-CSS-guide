# **Introduction to Web Dev**

Front End Journey 101 Memos

<img style="width:400px;" src="https://camo.githubusercontent.com/cae12fddd9d6982901d82580bdf321d81fb299141098ca1c2d4891870827bf17/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f313336302f302a37513379765349765f7430696f4a2d5a2e676966" alt="Programming is my life~"/>

---

## Table of Content

- [Introduction](#introduction)

  - [HTML basics](#html-basics)

    - [HTML tags](#html-tags)

    - [Head Section](#head-section)

    - [Text](#text)

    - [Entities](#entities)

    - [Hyperlinks](#hyperlinks)

    - [Images](#images)

    - [Video and Audio](#video-and-audio)

    - [Lists](#lists)

    - [Tables](#tables)

    - [Containers](#containers)

    - [Semantic Elements](#semantic-elements)

    - [Basic structure of a web page](#basic-structure-of-a-web-page)
    - [Summary](#summary)

  - [CSS basics](#css-basics)

    - [Providing CSS](#providing-css)

    - [Normalizing CSS](#normalizing-css)

    - [Basic Selectors](#basic-selectors)

    - [Relational selectors](#relational-selectors)

    - [Pseudo-class Selectors](#pseudo-class-selectors)

  - [Development tools](#development-tools)

---

### Introduction

Today is an exciting day (Nov. 28 2021) as I officially launched my Front End learning Journey.

I am taking this memos as I go through the journey to take down all the important concepts that I learned using MarkDown language.

The journey path will be :

1. HTML & CSS
2. JavaScript
3. React
4. Git
5. ... other increble awesomeness ...

With all the passions, let's dive right in ! ᕙ(`▿´)ᕗ

### _The inspiration quote for today:_

    We can always kind of be average and do what's normal. I am not in this to do what's normal.
                                                --Kobe Bryant

---

### HTML basics

To start with, first thing to do is to pick your fav text editor. I will be using VS code throughout the entire journey.

Apart from VS code, we also need 2 extensions to help us code HTML more efficiently:

- **Live Server** (immediately see the changes after saving)
- **Prettier - Code formatter** (automatically align the code)

---

Now create a new HTML file called `index.html`
(Note: `index` indicates home page)

First thing to type after creating a HTML file is :

```html
<!DOCTYPE html>
<html>
  <!-- To be continue... -->
</html>
```

Note:

- `DOCTYPE` represents HTML 5 Document Type Decoration
- HTML is **NOT** a case sensitive language. Both `DOCTYPE` and `doctype` will work
- HTML is **NOT** a indentation sensitve language since most tags contain opening tag `<html>` and closing tag `</html>`

---

#### HTML tags

In the simple web page, just like a human, it must contain _head_ and _body_.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My first web page</title>
  </head>
  <body>
    <img src="images/doggy.jpg" alt="" />
    <p>@Paul Lu</p>
    <p>I love Frontend Dev</p>
  </body>
</html>
```

In the case above, we have created the _head_ by have `<head> ... </head>`

and the _body_ with `<body> ... </body>`

- `<title>` indicates the name of the tab in your browser.
- `<p>` indicates plain text.
- `<img>` is a special tag as it doesn't have closing tag. i.e. `</img>`.
  It has 2 parameters:
  - `src=` the image location (_source_)
  - `alt=` display if the image fails to display, name of the image (_alternative_)

---

#### Head section

When we create a blank html file, we can quickly generate a boilerplate by pressing `!` + `tab`

Your boilerplate might look different than mine, this is what my boilerplate looks like:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

Notice that there are several `<meta>` tags showing up inside the `<head>` section.

- `<meta>` tag defines metadata about an HTML document. Metadata is data (information) about data.
- `charset` stands for _character set_, `UTF-8` is the standard character encoding you should use in your web pages.
- `X-UA-Compatible` specifies the document mode for Internet Explorer. `IE=edge` is the highest supported mode.
- `viewport` renders the width of the page to the width of the device's screen size.

You can also add some more `<meta>` tags to your head section, such as:

```html
<!-- Define keywords for search engines: -->
<meta name="keywords" content="HTML, CSS" />
<!-- Define a description of your web page: -->
<meta name="description" content="Awesome HTML Memo" />
<!-- Define the author of a page: -->
<meta name="author" content="Paul Lu" />
```

---

#### Text

Now that we know the basic way to display text in html page,

for instance:

```html
<body>
  <p>I love web dev!</p>
</body>
```

##### _Emphasis_

You can emphasize the text by wrapping it with `<em>` tag like so:

```html
<p>I love <em>web dev</em> !</p>
```

By default, your emphasized word will be italic like so:

<p>I love <em>web dev</em> !</p>

**Tips**: `shift` + `cmd` + `p` to open Command Palette, type `wrap`, and enter the name of the tag (e.g. `em`) to wrap selected text with tags.

Yet you can customize your own `<em>` tag in styling section.

```html
<style>
  em {
    color: red;
    font-style: normal;
  }
</style>
```

Note: As your code getting larger, you should always keep your html having **TEXT ONLY** and move all your styling to your CSS file.

##### _Heading_

Creating different levels of heading by simply making `<h#>` tag.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
```

> <h1>Heading 1</h1>
> <h2>Heading 2</h2>
> <h3>Heading 3</h3>

Note: You should **ALWAYS** use heading based on their hierarchy instead of their size since the size can be changed in CSS.

---

#### Entities

A character entity is a code used to represent a character that doesn't belong to the document's character set.

To display `<` and `>` in html, you have to use `&lt;` and `&gt;`, otherwise html will assume these are indicating tags.

```html
<p>I love &lt;html&gt; !</p>
```

<p>I love &lt;html&gt; !</p>

[More Entities Reference HERE !](https://dev.w3.org/html5/html-author/charref)

---

#### Hyperlinks

HTML links are hyperlinks.

You can click on a link and jump to another document.

When you move the mouse over a link, the mouse arrow will turn into a little hand.

==Note: A link does not have to be text. A link can be an image or any other HTML element!==

You can create a hyperlink by simply pressing `a`+ `tab`

```html
<a href="LINK_ADDRESS">OBJECT_TO_BE_DISPLAYED</a>
```

Object doesn't necessarily means text, it can also mean an image:

<!-- <a href="/content/about.html">
      <img src="/images/doggy.jpg" alt="" />
    </a> -->

```html
<a href="/content/about.html">
  <img src="/images/doggy.jpg" alt="" />
</a>
```

In the link address section, you can define your address in multiple way

##### _Relative URL_

A relative URL specifies the target resource relative to the current resource.

Under the same folder:

```html
<a href="about.html">About Me </a>
```

Under the sub folder :

```html
<a href="content/about.html">About Me </a>
```

Under the root folder (1 level) :

```html
<a href="../about.html">About Me </a>
```

Under the root folder (3 level) :

```html
<a href="../../../about.html">About Me </a>
```

##### _Absolute URL_

An absolute URL specifies the location of a resource irrespective of the current resource. It can start with a `/` to indicate the root of the website or a protocol (eg `http://`) to represent a resource on a different website.

```html
<!-- Relative URL -->
<a href="../../../about.html">About Me </a>

<!-- Absolute URL -->
<a href="/content/about.html"></a>
```

##### _Heading URL_

If you want to jump to the beginning of a specific heading section, you can make it link to a specific heading ID.

First by defining an ID to the heading:

```html
<h2 id="section-css">CSS</h2>
```

Then add `#` before the heading ID in your hyperlink to indicate it's a Heading URL:

```html
<a href="#section-css">CSS</a>
```

Conversely, you can jump back to the top of the page by simply linking to a `#`

```html
<a href="#">Jump to the top</a>
```

##### _Image URL_

To link to an image file by providing the image path:

```html
<a href="images/doggy.jpg">Picture</a>
```

Additionally, you can make the image downloadable by specifying `download`

```html
<a href="images/doggy.jpg" download>Picture</a>
```

##### _Web Page URL_

Use a full URL to link to a web page:

```html
<a href="https://google.com">Google</a>
```

By default, the linked page will be displayed in the current browser window. To change this, you must specify another target for the link.

Use target="\_blank" to open the linked document in a new browser window or tab:

```html
<a href="https://google.com" target="_blank">Google</a>
```

[HTML Hyperlinks](https://www.w3schools.com/html/html_links.asp)

---

#### Images

[How to insert an image](#html-tags)

To better fit an image into html page, you might need to modify its size.

```html
<style>
  img {
    /* change the width and height */
    width: 200px;
    height: 200px;

    /* the image will not be squashed */
    object-fit: cover;
  }
</style>
```

[Free Images Website](https://unsplash.com/)

---

#### Video and Audio

To Insert a video clip is simple, just like an image.

```html
<video src="LINK_ADDRESS">ALT_MESSAGE</video>
```

Some browsers doesn't support videos, hence you must specify `ALT_MESSAGE` to show the message if it doesn't work:

```html
<video src="/videos/ocean.mp4">Your browser doesn't support videos.</video>
```

[Browsers that support video display](https://caniuse.com/)

You can add some boolean value to make it have a play buttom `controls`, autoplay `autoplay` and looping `loop`:

```html
<video controls autoplay loop src="/videos/ocean.mp4">
  Your browser doesn't support videos.
</video>
```

Audio Implementation is the same as Video but with `<video>` replaced by `<audio>`

```html
<audio controls autoplay loop src="/audios/music.mp4">
  Your browser doesn't support audios.
</audio>
```

[Free Videos Website](https://www.pexels.com/)

---

#### Lists

HTML lists allow web developers to group a set of related items in lists.

##### _Unordered Lists_

An unordered list starts with the `<ul>` tag. Each list item starts with the `<li>` tag.

The list items will be marked with bullets (small black circles) by default:

```html
<!-- Unordered Lists -->
<ul>
  <li>
    Courses
    <ul>
      <li>HTML</li>
      <li>JavaScript</li>
      <li>Git</li>
    </ul>
  </li>
  <li>School</li>
  <li>Major</li>
  <li>Contact me</li>
</ul>
```

Output:

<ul>
  <li>
    Courses
    <ul>
      <li>HTML</li>
      <li>JavaScript</li>
      <li>Git</li>
    </ul>
  </li>
  <li>School</li>
  <li>Major</li>
  <li>Contact me</li>
</ul>

> Tips: type `ul>li*3` to quickly generate an unordered list with 3 list items.

Note: You can customize your bullet points, like so:

```html
<style>
  ul {
    /* make bullet points squared */
    list-style-type: square;
  }
</style>
```

##### _Ordered Lists_

An ordered list starts with the `<ol>` tag. Each list item starts with the `<li>` tag.

The list items will be marked with numbers by default:

```html
<!-- Ordered Lists -->
<ol>
  <li>Preheat the oven.</li>
  <li>Place the ingrident on the crust.</li>
  <li>Put the pizza in the oven for 20 mins</li>
</ol>
```

Output:

<ol>
  <li>Preheat the oven.</li>
  <li>Place the ingrident on the crust.</li>
  <li>Put the pizza in the oven for 20 mins</li>
</ol>

##### _Description Lists_

A description list is a list of terms, with a description of each term.

The `<dl>` tag defines the description list, the `<dt>` tag defines the term (name), and the `<dd>` tag describes each term:

```html
<!-- Description List -->
<dl>
  <dt>Name</dt>
  <dd>Paul Lu</dd>
  <dt>Major</dt>
  <dd>Computer Science</dd>
  <dt>Skills</dt>
  <dd>HTML</dd>
  <dd>CSS</dd>
  <dd>JavaScript</dd>
</dl>
```

Output:

<dl>
  <dt>Name</dt>
  <dd>Paul Lu</dd>
  <dt>Major</dt>
  <dd>Computer Science</dd>
  <dt>Skills</dt>
  <dd>HTML</dd>
  <dd>CSS</dd>
  <dd>JavaScript</dd>
</dl>

---

#### Tables

HTML tables allow web developers to arrange data into rows and columns.

To create a simple table, we need `<table>`, `<tr>`, `<td>`. (or simply `table>tr>td*2`)

```html
<table>
  <tr>
    <td>Marketing</td>
    <td>$200</td>
  </tr>

  <tr>
    <td>Accounting</td>
    <td>$100</td>
  </tr>
</table>
```

You can add headers on each columns by replacing `<th>` with `<tr>`

```html
<table>
  <tr>
    <th>Category</th>
    <th>Amount</th>
  </tr>
</table>
```

Adding footer by using `<tfoot>`:

```html
<tfoot>
  <tr>
    <th>Total</th>
    <th>$300</th>
  </tr>
</tfoot>
```

Style your table so it looks prettier:

```html
<style>
  /* Apply styling on all three tags */
  table,
  td,
  th {
    /* Thin solid gray border */
    border: 1px solid gray;
    /* collapse the line in between each cell */
    border-collapse: collapse;
    /* make element far away from the border */
    padding: 5px;
  }

  tfoot {
    text-align: left;
  }
</style>
```

Note: In order to make searching engine quickly locate your tag, you must use `<thead>`, `<tbody>` and `<tfoot>` and organize your code:

```html
<table>
  <!-- thead section -->
  <thead>
    <tr>
      <!-- merge 2 rows -->
      <th colspan="2">Expenses</th>
    </tr>
    <tr>
      <th>Category</th>
      <th>Amount</th>
    </tr>
  </thead>

  <!-- tbody section -->
  <tbody>
    <tr>
      <td>Marketing</td>
      <td>$200</td>
    </tr>

    <tr>
      <td>Accounting</td>
      <td>$100</td>
    </tr>
  </tbody>

  <!-- tfoot section -->
  <tfoot>
    <tr>
      <th>Total</th>
      <th>$300</th>
    </tr>
  </tfoot>
</table>
```

Output:

<style>
  table,
  td,
  th {
    border: 1px solid gray;
    border-collapse: collapse;
    padding: 5px;
  }

  tfoot {
    text-align: left;
  }
</style>

<table>
  <thead>
    <tr>
      <th colspan="2">Expenses</th>
    </tr>
    <tr>
      <th>Category</th>
      <th>Amount</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Marketing</td>
      <td>$200</td>
    </tr>

  <tr>
    <td>Accounting</td>
    <td>$100</td>
  </tr>
  </tbody>

  <tfoot>
    <tr>
      <th>Total</th>
      <th>$300</th>
    </tr>
  </tfoot>
</table>

---

#### Containers

The container class is the perfect class to use for all HTML container elements like:

`<div>`, `<article>`, `<section>`, `<header>`, `<footer>`, `<form>`, and more.

##### Block-level Elements

A block-level element always starts on a new line.

A block level element has a top and a bottom margin, whereas an inline element does not.

The `<div>` element is a block-level element.

Ex:

```html
<div>
  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>

  <a href="#">Link</a>
</div>
```

If we style `<div>`, the entire `<div>` block will be affected, which is not good sometimes.

```html
<style>
  div {
    background-color: yellow;
  }
</style>
```

One way of addressing this issue is to set different class for `<div>`.

```html
<style>
  /* omit div to generalize all container that has product class will be affected. */
  .product {
    background-color: yellow;
  }
</style>

<!-- define a product class to this div container -->
<div class="product">
  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>

  <a href="#">Link</a>
</div>
```

##### In-line Elements

An inline element does not start on a new line.

An inline element only takes up as much width as necessary.

If we want to highlight some words in the sentence without change to a new line, we can use in-line element, `<span>`.

```html

<style>
  .highlight {
    background-color: yellow;
  }
</style>

<p>
  <div>
    <span class="highlight">Lorem</span> ipsum dolor, sit amet consectetur
    adipisicing elit.
  </div>
</p>
```

---

#### Semantic Elements

Semantic Elements make our html element more readable and more meaningful for the search engine.

Generic Elements: `<div>`, `<span>`

Semantic Elements: `<article>`, `<figure>`, `<mark>`, `<time>` etc.

##### Article

we use `<article>` to wrap up any self-contain content like Forum post, comments, Reviews

```html
<article class="article">
  <h1>Heading1</h1>
  <p>
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Reprehenderit nemo
  </p>
</article>
```

##### Figure

Use a `<figure>` element to mark up a photo in a document, and a `<figcaption>` element to define a caption for the photo:

```html
<figure>
  <img src="" alt="" />

  <!-- figure caption under the image -->
  <figcaption>My Coffee this morning</figcaption>
</figure>
```

##### Mark

Use a `<make>` to replace `<span class=highlight>` to automatically highlight text in yellow.

```html
<!-- 'Lorem' is highlighted in yellow -->
<p><mark>Lorem</mark> ipsum, dolor sit amet consectetur adipisicing elit.</p>
```

##### Time

Use a `<Time>` to specify time to help search engines quickly extract time from the text.

```html
<p>
  <!-- datetime="YYYY-MM-DD 24:HR" -->
  Published
  <time datetime="2021-01-01 17:00">January 1 2022 05:00pm</time>
</p>
```

---

#### Basic structure of a web page

Now that we know some semantic elements as well as some genertic elements, there is a general layout for you to structure every web page.

==Note: Structure may vary in different scenarios==

To begin with, each web page must have `header`, `main`, `footer` sections. It might also have `aside` section to display some content aside from the main content.

For each section, it will also contain other sections or elements that we learned before.

Example:

```html
<body>
  <!-- Header Section -->
  <header>
    <!-- Nav Bar -->
    <nav>
      <!-- Unordered List -->
      <ul>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </nav>
  </header>
  <!-- Main Section -->
  <main>
    <!-- Several Sections -->
    <section>
      <!-- Header inside each section -->
      <h2>Products</h2>
      <!-- Several Article inside a section -->
      <article></article>
      <article></article>
      <article></article>
    </section>
    <section>
      <h2>Testimonial</h2>
      <article>
        <!-- Several Sections inside an article -->
        <section></section>
        <section></section>
      </article>
      <article></article>
    </section>
  </main>
  <!-- Aside Section -->
  <aside></aside>
  <!-- Footer Section -->
  <footer>
    <nav>
      <ul>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </nav>
  </footer>
</body>
```

---

#### Summary

- The `<head>` section is used to provide information about a webpage.
- The `<p>` element is used to represent a paragraph. A paragraph can be one or many
  lines of text.
- The `<em>` element is used to define emphasized text. By default, emphasized text is
  displayed in _italic_.
- The `<strong>` element is used to represent important content. Browsers, by default,
  render strong content in **bold**.
- The`<i>`and `<b>` elements are considered deprecated because HTML should not be
  used for styling. That’s the role of CSS.
- Headings are represented using `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`. Every
  web page should have one and only one `<h1>` element. Headings should have a natural
  hierarchy and should not be skipped.
- Entities are used to display special characters such as angle brackets, copyright symbol,
  etc. The most important entities are: `&nbsp;` (non-breaking space), `&lt;` (less than
  sign), `&gt;` (greater than sign) and `&copy;` (copyright symbol).
- The `<a>` (anchor) element, with its href attribute, is used to create a hyperlink to web
  pages, locations in the same page, files and email addresses.
- A relative URL specifies the target resource relative to the current resource. An absolute
  URL specifies the location of a resource irrespective of the current resource. It can start
  with a / to indicate the root of the website or a protocol (eg http://) to represent a
  resource on a different website.
- The `<img>` element is used to display an image. It’s a common best practice to set the
  alt (alternative text) attribute. This helps visually impaired people understand the page
  content. Also, if the image cannot be loaded, the alternative text is displayed.
- The `<video>` and `<audio>` elements are used to display video and audio. These
  elements have boolean attributes such as controls, autoplay and loop.
- The `<ul>` element is used to represent a list where the order of items doesn’t matter. The
  `<ol>` element is used to represent an ordered list of items. The `<dl>` (description list)
  element is used to implement a glossary or to display metadata.
- The `<table>` element should only be used to represent tabular data. A table can have
  zero or more `<tr>` (table row) elements. Each `<tr>` element can have zero or more cells.
  Cells can be data cells (`<td>`) or header cells (`<th>`).
- The `<div>` and` <span>` elements are generic containers used for styling purposes. Divs
  are block-level elements, spans are inline elements. A block-level element starts on a new
  line and takes up the entire available horizontal space.
- Semantic elements help us write markup that is more meaningful and descriptive to
  search engines, screen readers and other software. So, use `<div>` and `<span>` elements
  when no other semantic element is appropriate.
- The semantic elements in HTML5 are: `<header>`, `<footer>`, `<nav>`, `<main>`,
  `<aside>`, `<article>`, `<section>`, `<figure>`, `<time>` and `<mark>`.

---

### CSS basics

After we created the "backbone" of the web, let's arrange these elements so they look prettier.

To accomplish this, CSS will be the "designer". (─‿‿─)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My first web page</title>
    <style>
      img {
        width: 100px;
        border-radius: 20px;
        float: left;
        margin-right: 10px;
      }

      p.username {
        font-weight: bold;
      }
    </style>
  </head>
  <body>
    <img src="images/doggy.jpg" alt="" />
    <p class="username">@Paul Lu</p>
    <p>I love Frontend Dev</p>
  </body>
</html>
```

Again, a few things to note:

- `<style> ... </style>` should appear inside the _head_ tag. Later on CSS file should be separated if too large.
- `TAGNAME {...}` to specify the tag you want to style.
- If the tag is too general, (e.g. `<p>` can indicates any text) inside the tag, add arg: `class=` to indicate its specific `ID`. Next, inside style sheet, `TAGNAME.ID` to refer to the particular tag.

---

#### Providing CSS

CSS can be provided through different ways:

##### Embedded stylesheets

Adding `<style>` in `<head>` section

```html
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
```

##### External stylesheets

Creating an external `.css` file and linking it to html

```css
/* CSS file */
p {
  color: grey;
}
```

```html
<!-- HTML file -->
<head>
  <link rel="stylesheet" href="style.css" />
</head>
```

##### Inline styles

Styling inside an independent tag

```html
<body>
  <p style="color: blue; font-weight: bold">Lorem ipsum dolor sit amet.</p>
</body>
```

==Note: This is NOT recommanded since it difficult to modify later==

Instead, we can use `id` or `class` to specify a tag:

```html
<head>
  <style>
    /* styling ID */
    #first {
      color: palegreen;
      font-weight: bold;
    }
    /* styling Class */
    .second {
      color: wheat;
      font-weight: bold;
    }
  </style>
</head>

<body>
  <p id="first">Lorem ipsum dolor sit amet.</p>
  <p class="second">Lorem ipsum dolor sit amet.</p>

  <p>Lorem ipsum dolor sit amet.</p>
</body>
```

==Note: `id` **MUST** be unique, whereas `class` doesn't necessarily.==

---

#### Normalizing CSS

Different browsers might render CSS differently. Some browsers version sometimes DO NOT support load the CSS feature.

Hence, we need use [Normailize.css](https://necolas.github.io/normalize.css/)

Download `normailze.css` and link to your html file so any browser can render your CSS features.

---

#### Basic Selectors

When we style different tags, we can catogorize them by `class` and `id`, which is commonly used in CSS.

==FYI: `#ID{..}` to style id, `.CLASS{..}` to style class.==

You can also choose to use "Wildcard" to select tags.

Ex:

```html
<!-- Html -->
<a href="https://www.google.com" target="_blank">Google</a>
```

There are multiple ways to specify this hyperlink using wildcard:

```css
/* CSS */

/* If the anchor has "target" attribute */
a[target] {
  color: orange;
}

/* If the anchor's "target" attribute is set to "_blank" */
a[target="_blank"] {
  color: orange;
}

/* If "href" is "https://www.google.com"  (This is Fragile!) */
a[href="https://www.google.com"]
{
  color: orange;
}

/* If "href" contains "google" */
a[href*="google"] {
  /* '*=' -> contain */
  color: orange;
}

/* If "href" starts with "https" */
a[href^="https"] {
  /* '^=' -> start with */
  color: orange;
}

/* If "href" ends with ".com" */
a[href$=".com"] {
  /* '$=' -> end with */
  color: orange;
}
```

---

#### Relational selectors

A CSS selector can contain more than one simple selector. Between the simple selectors, we can include a combinator.

There are four different combinators in CSS:

- descendant selector (space)
- child selector (>)
- adjacent sibling selector (+)
- general sibling selector (~)

Ex: say we have a html like this:

```html
<section id="products">
  <!-- p1 -->
  <p>Lorem ipsum dolor sit amet.</p>

  <article>
    <!-- p2 -->
    <p>Lorem ipsum dolor sit amet.</p>
  </article>
</section>
<!-- p3 -->
<p>Lorem ipsum dolor sit amet.</p>
<!-- p4 -->
<p>Lorem ipsum dolor sit amet.</p>
```

_Determine which `<p>` will be affected by CSS after each selector._

##### descendant selector (space)

The descendant selector matches all elements that are descendants of a specified element.

The following example selects all `<p>` elements inside `#products` id:

```css
/* Selecting all <p> in products */
#products p {
  background-color: yellow;
}
```

==p1 & p2 will be affected==

##### Child Selector (>)

The child selector selects all elements that are the children of a specified element.

The following example selects all `<p>` elements that are children of a `#products` id:

```css
/* Selecting all <p> that are the direct children of product */
#products > p {
  background-color: yellow;
}
```

==Only p1 will be affected==

##### Adjacent Sibling Selector (+)

The adjacent sibling selector is used to select an element that is directly after another specific element.

Sibling elements must have the same parent element, and "adjacent" means "immediately following".

The following example selects the first `<p>` element that are placed immediately after `#products` id:

```css
/* Selecting only the first <p> coming right after product  */
#products + p {
  background-color: yellow;
}
```

==Only p3 will be affected==

##### General Sibling Selector (~)

The general sibling selector selects all elements that are next siblings of a specified element.

The following example selects all `<p>` elements that are next siblings of `#products` id:

```css
/* Selecting all <p> after product */
#products ~ p {
  background-color: yellow;
}
```

==p3 & p4 will be affected==

Note: Relational selectors can be fragile if the order of the tag is mutated.

---

### Pseudo-class Selectors

A pseudo-class is used to define a special state of an element.

For example:

Let's say we want to style the first `<p>` in the article only.

```html
<!-- 2 paragraphs in an article section -->
<article>
  <p class="first">Lorem ipsum dolor sit amet.</p>

  <p>Lorem ipsum dolor sit amet.</p>
</article>
```

Without Pseudo-class, we can define a class of the first `<p>`:

```css
/* Without using Pseudo-class Selectors */
/* You can specify first <p> by defining a class */
.first {
  font-size: 140%;
  font-style: italic;
}
```

By using Pseudo-class, we use `:` to specify the relationship:

```css
/* first-child inside article class */
article :first-child {
  font-size: 140%;
  font-style: italic;
}
```

However, this type of pseudo class selector is fragile. If we change the first element of article, the rule will break.

To address this issue, we can use `first-of-type` selector

```css
/* the first occurance of any type inside the article */
article :first-of-type {
  font-size: 140%;
  font-style: italic;
}
```

If we only want to style the first occurance of `<p>`, we can be more specific:

```css
/* the first occurance of <p> inside the article */
article p:first-of-type {
  font-size: 140%;
  font-style: italic;
}
```

Similarily, we can also apply the rule on `last-of-type`:

```css
/* the last occurance of <p> inside the article */
article p:last-of-type {
  font-weight: bold;
}

/* the last child of <p> inside the article */
article p:last-child {
  font-weight: bold;
}
```

##### Pseudo-class selector on unordered lists:

To select specify rows of an unordered lists:

```html
<!-- An unordered list containing 5 items -->
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
  <li>Item 5</li>
</ul>
```

```css
/* Select odd rows */
ul li:nth-child(odd) {
  color: deeppink;
}

/* Select even rows */
ul li:nth-child(even) {
  color: deeppink;
}

/* Select 3 multiple rows */
ul li:nth-child(3n) {
  color: deeppink;
}
```

##### Pseudo-class selector on hyperlinks:

To style visited and unvisited links differently:

```css
/* visited link */
a:visited {
  color: darkcyan;
}

/* unvisited link */
a:link {
  color: purple;
}
```

To style links that are hovered by mouse or `tab` key:

```css
a:hover,
a:focus {
  color: deeppink;
}
```

[CSS Pseudo-classes](https://www.w3schools.com/css/css_pseudo_classes.asp)

---

####

---

### Development tools

If you encounter some issues with your HTML or CSS that your web page doesn't display the expected tag/style. It is difficult to _Debug_ your code since HTML & CSS doesn't mark up your bugs like other programming language.

Fortunately, there's some websites that can help with that ! ❤（っ＾ ▿ ＾）

[HTML Validation Site](https://validator.w3.org/#validate_by_upload)

[CSS Validation Site](https://jigsaw.w3.org/css-validator/#validate_by_upload)

For example:

After uploading our HTML file, we might receive a warning message like this:
![Warning Message](images/warning.png)
This means the code works fine in local server, but if it is on remote server, it will cause some issues since the language isn't declared. To get around this, let's simply add `lang="en"` after `<html>` openning tag.

Now the code should look like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>My first web page</title>
    <style>
      img {
        width: 100px;
        border-radius: 20px;
        float: left;
        margin-right: 10px;
      }

      .username {
        font-weight: bold;
      }
    </style>
  </head>
  <body>
    <img src="images/doggy.jpg" alt="" />
    <p class="username">@Paul Lu</p>
    <p>I love Frontend Dev</p>
  </body>
</html>
```

---

### Keyboard shortcut for Mac

`shift + option + down` to duplicate block of code

`shift + up/down` to select multiple lines of code

`option + up/down` to move selected code up/down

`cmd + d` to show 2 cursors to replace a name with 2 selected variable

Zen Coding:
`section>ul>li*3{Item $}` + `tab` =

```html
<section>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
</section>
```

`section#products` + `tab` = `<section id="products"></section>`

`section.products` + `tab` = `<section class="products"></section>`
