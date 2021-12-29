# **Front End Journey Memos**

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
    - [Summary](#1summary)
  - [CSS basics](#css-basics)
    - [Providing CSS](#providing-css)
    - [Normalizing CSS](#normalizing-css)
    - [Basic selectors](#basic-selectors)
    - [Relational selectors](#relational-selectors)
    - [Pseudo-class selectors](#pseudo-class-selectors)
    - [Pseudo-element selectors](#pseudo-element-selectors)
    - [Inheritance](#inheritance)
    - [Color](#color)
    - [Gradients](#gradients)
    - [Borders](#borders)
    - [Shadows](#shadows)
    - [Summary](#2summary)
    - [CSS Cheat Sheet](#css-cheat-sheet)
  - [Development tools](#development-tools)
- [Intermediate](#intermediate)
  - [Layout](#layout)
    - [The box model](#the-box-model)
    - [Sizing elements](#sizing-elements)
    - [Overflowing](#overflowing)
    - [Measurement units](#measurement-units)
    - [Positioning](#positioning)
    - [Floating elements](#floating-elements)
    - [Flexbox](#flexbox)
    - [Grid](#grid)
    - [Hiding elements](#hiding-elements)
    - [Media queries](#media-queries)
  - [Typography](#typography)
  - [Images](#images)
  - [Forms](#forms)
  - [Transformations, Transitions, and Animations](#transformations-transitions-and-animations)
  - [Writing Clean, Maintainable CSS](#writing-clean-maintainable-css)
  - [Layout](#Layout)

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

<h4 id="1summary">Summary</h4>

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

### Pseudo-class selectors

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

#### Pseudo-element selectors

A CSS pseudo-element is used to style specified parts of an element.

For example, it can be used to:

- Style the first letter, or line, of an element
- Insert content before, or after, the content of an element

Ex: Say you want to bold the first letter of the paragraph

Without using Pseudo-element selectors, you must make a `span` `class` and style that class:

```html
<!-- Without using Pseudo-element selectors -->
<style>
  /* Style specific class */
  .first-letter {
    font-size: 140%;
    font-weight: bold;
  }
</style>

<p>
  <span class="first-letter">L</span>orem ipsum dolor sit, amet consectetur
  adipisicing elit. Non quos est exercitationem tempora, possimus, iste a
  tempore odit corporis ipsa doloremque fuga veniam repellat esse provident sit
  dicta, dolorem dignissimos.
</p>
```

Thanks to Pseudo-element selectors, the previous step is unnecessary.

Instead, you should use `::` to indicate a Pseudo-element:

```css
/* style first letter of each <p> */
p::first-letter {
  font-size: 140%;
  font-weight: bold;
}

/* style first line of each <p> */
p::first-line {
  font-weight: bold;
}

/* Style the background color of cursor selection */
::selection {
  background-color: pink;
}

/* insert a Pseudo-element before <p> */
p::before {
  content: "...";
  /* set it to block element that takes the entire block */
  display: block;
}
```

[CSS Pseudo-elements](https://www.w3schools.com/css/css_pseudo_elements.asp)

---

#### Pseudo-elements VS. Pseudo-classes

**Pseudo-elements** is used to style _part of an element_, such as `first-letter`, `first-line`.

**Pseudo-classes** is used to style elements _in a particular state_, such as `Hovered anchor`.

---

#### Selectors Specificty

If there are two or more conflicting CSS rules that point to the same element, the browser follows some rules to determine which one is most specific and therefore wins out.

Specificity Hierarchy:

**Inline styles** - An inline style is attached directly to the element to be styled. Example: `<h1 style="color: #ffffff;">`. _(Weight = 1000)_

**IDs** - An ID is a unique identifier for the page elements, such as `#navbar`. _(Weight = 100)_

**Classes, attributes and pseudo-classes** - This category includes .classes, `[attributes] `and pseudo-classes such as `:hover`, `:focus` etc. _(Weight = 10)_

**Elements and pseudo-elements** - This category includes element names and pseudo-elements, such as `h1`, `div`, `:before` and `:after`. _(Weight = 1)_

For example:

```html
<body>
  <section>
    <!-- a paragraph containing class and id -->
    <p class="text" id="first-line">Lorem ipsum dolor sit, amet</p>

    <!-- inline styling, top priority! -->
    <p style="color= green;">Lorem ipsum dolor sit, amet</p>
  </section>
</body>
```

```css
/* General Element, Weight: 0, 0, 1 */
p {
  color: pink;
}

/* Class, Weight: 0, 1, 0 */
.text {
  color: red;
}

/* ID, Weight: 1, 0, 0 */
#first-line {
  color: blue;
}

/* ID + Class Weight: 1, 1, 0 */
.text#first-line {
  color: blueviolet;
}
```

In the case above, the text color should be `blueviolet` since it hold the most weight.

==Note: Be aware not to be too specific about your specificty since it may leave a mess==

---

#### Inheritance

In CSS, inheritance controls what happens when no value is specified for a property on an element.

CSS properties can be categorized in two types:

- **inherited properties** (e.g font, color)

- **non-inherited properties** (e.g border)

For example:

```html
<!-- a <p> with a word wrapped with <strong> -->
<body>
  <p>Lorem ipsum <strong>dolor</strong> sit amet.</p>
</body>
```

If we style the color of `<p>`, the color of `<strong>` will inherit from it,

But the border will not be inherited since it is a non-inherited property:

```css
p {
  /* color will be inherited to <strong> */
  color: dodgerblue;

  /* border will NOT be inherited to <strong> */
  border: 1px solid black;
}
```

However, if you are unhappy about it :persevere:, you can also manually set inherited properities.

```css
strong {
  /* set the color back to initial (black) */
  color: initial;

  /* Force it to inherit the border properity */
  border: inherit;
}
```

---

#### Color

Finally comes to my favourite part - Color !!! :heart_eyes:

In CSS, colors can be represented in several ways:

- **Named colors** (e.g `yellow`, `blue`)
- **RGB** (e.g `60, 143, 82`)
- **HSL** (e.g `136, 58%, 56%`) _- (Hue-Saturation-Lightness)_
- **Hexadecimal** (e.g. `#3c8f52`)

Ex:

```css
/* Define a box filled in with color */

/* By Named colors */
.box {
  width: 200px;
  height: 200px;
  background-color: yellow;
}

/* By RGB (range from 0~255) */
.box {
  width: 200px;
  height: 200px;
  background-color: rgb(75, 176, 44);
}

/* By RGBA ('a' short for Alpha, meaning transparency between 0~1) */
.box {
  width: 200px;
  height: 200px;
  background-color: rgba(75, 176, 44, 0.5);
}

/* By Hexadecimal */
.box {
  width: 200px;
  height: 200px;
  background-color: #4bb02c;
}

/* By hsl */
.box {
  width: 200px;
  height: 200px;
  background-color: hsl(106, 60%, 43%);
}

/* By hsla ('a' short for Alpha, meaning transparency between 0~1)*/
.box {
  width: 200px;
  height: 200px;
  background-color: hsla(106, 100%, 43%, 0.5);
}
```

Note: By convention, `hexadecimal` is the most popular way to use, but it doesn't support `Alpha` channel. If you prefer to adjust the color shadow and brightness like me, then `hsl` is a better choice.

> Tips: You can always google [Color Picker](https://g.co/kgs/mdQdSF) to pick your ideal color.

---

#### Gradients

CSS gradients let you display smooth transitions between two or more specified colors.

CSS defines three types of gradients:

- Linear Gradients (goes down/up/left/right/diagonally)
- Radial Gradients (defined by their center)
- Conic Gradients (rotated around a center point)

Syntax:

`background-image: linear-gradient(direction, color-stop1, color-stop2, ...); `

For example:

```css
/* By default, the gradient goes from top to bottom  */
.box {
  width: 200px;
  height: 200px;
  background: linear-gradient(dodgerblue, yellow);
}

/* Change direction from left to right */
.box {
  width: 200px;
  height: 200px;
  background: linear-gradient(to right, dodgerblue, yellow);
}

/* Direction starts from 45 deg, yellow starts from 30% */
.box {
  width: 200px;
  height: 200px;
  background: linear-gradient(45deg, dodgerblue, yellow 30%);
}
```

[CSS Gradient Generator](https://cssgradient.io/) can make your life easier.

---

#### Borders

The `border` property is a shorthand property for:

- **border-width**
- **border-style** (solid, dashed, dotted) REQUIRED!
- **border-color**

For example:

```css
.box {
  width: 800px;
  height: 400px;
  background: wheat;

  /* border: width style color */
  border: 10px dashed royalblue;
}
```

On top of that, you can also specify the direction of the border

==Note: the order matters==

Ex:

```css
.box {
  width: 800px;
  height: 400px;
  background: wheat;
  border: 10px dashed royalblue;

  /* Set top border */
  border-top: 20px solid red;

  /* Set width for each side */
  border-width: 10px 20px 10px 20px; /* trbl (top right bottom left) */

  /* Make the border rounder */
  border-radius: 50px;
}
```

:boom::boom::boom: Wanna create a shape using border ?

[The shape of CSS](https://css-tricks.com/the-shapes-of-css/)

---

#### Shadows

With CSS you can add shadow to text and to elements.

- `text-shadow`

- `box-shadow`

```css
/* Text shadow */
h1 {
  /* horizontal 3px, vertical 3px, blur 5px, color */
  text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.2);
}

/* Box shadow */
.box {
  width: 800px;
  height: 400px;
  background: wheat;

  /* set the shadow right in the center */
  box-shadow: 0 0 30px grey;
}
```

---

<h4 id="2summary">Summary</h4>

- CSS styles can be embedded in an HTML document, written in a separate file (as an external stylesheet) or written inline in an HTML element using the `style` attribute.

- Inline styles overwrite embedded styles which in turn overwrite external styles.

- External stylesheets provide the best separation of HTML and CSS code and result in more maintainable code. Plus, an external stylesheet can be used in many HTML documents.

- We can select elements by their type, class, attribute or ID.

- Relational selectors help us select elements without the need to assign them a specific ID or class. This, however, can result in fragile styles. If we move elements around, our CSS rules may break. We can still use them in situations where we are certain about the location of elements.

- We can take advantage of pseudo-classes to target elements without the need to give them a specific class. The most common pseudo-classes are: `first-child`, `first-of-type`, `last-child`, `last-of-type` and `nth-child`. Pseudo-classes start with a single colon `:`.

- With pseudo-elements we can style a part of an element. The most common pseudo- elements are: `first-letter`, `first-line`, `selection`, `before` and `after`. Pseudo-elements start with double colons `::`.

- Selectors specificity determines the weight of a selector. When multiple selectors target the same element, the browser applies the selector with the higher specificity (weight). If two selectors have the same specificity, the one that comes last is the winner.

- ID selectors are the most specific selectors because we cannot have multiple elements with the same ID. Class and attribute selectors are less specific because we can have many elements with the same class and/or attributes. Element selectors are the least specific selectors.

- In VSCode, we can see the specificity of a rule by hovering our mouse over it. The specificity is represented using three numbers (x, y, z) where x represents the number of ID selectors, y represents the number of class/attribute selectors and z represents the number of element selectors.

- Some CSS properties inherit their value from their parent element. Typically, properties that are used for styling text such as text color, font, font size, etc are inherited. We can stop the inheritance by setting the value of a property to `initial`. To enforce inheritance, we should set the value of a property to `inherit`.

- We can specify colors by their name, hexadecimal value, RGB/RGBA value or HSL/ HSLA value.

- RGBA and HSLA values include an alpha channel used for transparency. The value for the alpha channel is a decimal point number between 0 (completely transparent) and 1 (completely opaque).

- Using the `linear-gradient()` and `radial-gradient()` functions we can create gradients in CSS. Gradients are images so they cannot be used as the value of `background-color` property. We can use them as the value of `background-image` or `background` properties.

- The border property is a shorthand property for `border-top`, `border-right`, `border-bottom` and `border-left`. It takes three values: the thickness of the border, its style and its color.

- We also have specific properties like `border-width`, `border-style` and `border-color`. These properties take four values for the top, right, bottom and left borders.

- Using the `box-shadow` and `text-shadow` properties we can apply a shadow to elements and text. These properties take a few values. The first two values determine the horizontal and vertical distance of the shadow from the element. The third value (called blur radius) determines the softness of the border. We can specify the color as the fourth value.

---

#### CSS Cheat Sheet

| Basic Selectors     |                                      |
| ------------------- | ------------------------------------ |
| `article`           | All article elements                 |
| `.product`          | Elements with the product class      |
| `#products`         | The element with the ID of products  |
| `a[href=“...”]`     | Anchors with the given href          |
| `a[href*=“google”]` | Anchors whose href contains google   |
| `a[href^=“https”]`  | Anchors whose href starts with https |
| `a[href$=“.com”]`   | Anchors whose href ends with .com    |

| Relational Selectors |                                                      |
| -------------------- | ---------------------------------------------------- |
| `#products p`        | All p elements inside #products                      |
| `#products > p`      | All p elements that are direct children of #products |
| `#products + p`      | The p element immediately after #products (sibling)  |
| `#products ~ p`      | All p elements after #products (siblings)            |

| Pseudo-class Selectors     |                                                    |
| -------------------------- | -------------------------------------------------- |
| `article :first-child`     | The first child of article elements                |
| `article :first-of-type`   | The first occurrence of elements of different type |
| `article p:first-of-type`  | The first p element inside article elements        |
| `article :last-child`      |                                                    |
| `article :last-of-type`    |                                                    |
| `article :nth-child(odd)`  |                                                    |
| `article :nth-child(even)` |                                                    |

| Pseudo-element Selectors |                                                    |
| ------------------------ | -------------------------------------------------- |
| `p::first-letter`        | The first letter of every p element                |
| `p::first-line`          | The first line of every p element                  |
| `::selection`            | Any selected element                               |
| `p::before`              | To insert content before the content of p elements |
| `p::after`               | To insert content after the content of p elements  |

| Colors                    |                            |
| ------------------------- | -------------------------- |
| `#fcba03`                 | Hexadecimal value          |
| `rgb(252, 186, 3)`        | RGB value                  |
| `rgba(252, 186, 3, 0.5)`  | Semi-transparent RGB value |
| `hsl(44, 98%, 50%)`       | HSL value                  |
| `hsla(44, 98%, 50%, 0.5)` | Semi-transparent HSL value |

| Gradients                                                         |
| ----------------------------------------------------------------- |
| `background: linear-gradient(blue, yellow);`                      |
| `background: linear-gradient(to bottom right, blue, yellow);`     |
| `background: linear-gradient(45deg, blue, yellow);`               |
| `background: linear-gradient(45deg, blue, yellow 30%);`           |
| `background: radial-gradient(white, yellow);`                     |
| `background: radial-gradient(circle, white, yellow);`             |
| `background: radial-gradient(circle at top left, white, yellow);` |

| Borders                                                          |
| ---------------------------------------------------------------- |
| `border: 10px solid blue;`                                       |
| `border-width: 10px 20px 30px 40px; /* top right bottom left */` |
| `border-radius: 5px;`                                            |
| `border-radius: 100%; /* full circle */`                         |

| Shadows                                        |
| ---------------------------------------------- |
| `box-shadow: 10px 10px;`                       |
| `box-shadow: 10px 10px grey;`                  |
| `box-shadow: 10px 10px 5px grey;`              |
| `text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.2);` |

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

### Intermediate

Now that we have learned the basic syntax about HTML & CSS, it is time to hover to the next level. After completing this level, you should be able to build a functional website.

### _The inspiration quote for today:_

    Always remember that you are absolutely unique. Just like everyone else.
                                                --Margaret Mead

---

#### Layout

##### The box model

Each element has `content` < `padding` < `border` < `margin` area.

Tips: you can always inspect and adjust this box model in your browser.

==Be cautious about `padding` and `margin`==

Ex:

Say we want to set the margin between 2 `<p>` to `20px`:

```html
<p>Lorem ipsum dolor sit amet.</p>
<p>Lorem ipsum dolor sit amet.</p>
```

```css
p {
  /* margin between will be 40px */
  padding: 20px;
  margin: 0;
}

p {
  /* Margin collapsing, margin will be 20px */
  padding: 0;
  margin: 20px;
}
```

So you should always use `margin` to seperate elements, and use `padding` to add space between `content` and `border`

##### Sizing elements

Since every element has a box model, things get a little tricker when it comes to sizing.

For example, say we have a box `<div>` element:

```html
<body>
  <div class="box"></div>
</body>
```

```css
.box {
  /* define width and height for 200px each */
  width: 200px;
  height: 200px;

  /* define the color of the box */
  background-color: gold;

  /* add 20px padding and border */
  padding: 20px;
  border: 20px solid orange;
}
```

When you inspect the box in the browser, it turns out that the size of the box is `280x280` instead of `200x200`.

The reason for that is because `width` and `height` you defined indicates `content` box, it doesn't take `padding` and `border` into account. _(Margin doesn't affect the actual size)_

To address this issue, we can use `box-sizing` property, which by default is set to `content-box`.

```css
.box {
  box-sizing: border-box;
}
```

Note: if you want to apply this rule to all box elements, you can use `universal selector`, i.e. `*`
However, `*` doesn't apply to [Pseudo-element](#pseudo-element-selectors), i.e. `::before`, `::after` so you have to manually include them.

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

Another triky issue is that `<div>` is a block-level element, which means if 2 boxes are created, they will not be arranged onto a single line.

If we change `<div>` to a inline element, i.e.`<span>`:

```html
<body>
  <span class="box"></span>
  <span class="box"></span>
</body>
```

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* a 200x200 gold box */
.box {
  width: 200px;
  height: 200px;
  background-color: gold;
}

/* some text inside the box */
.box::before {
  content: "hello";
}
```

The `<span>` will disrespect the `width` and `height`, this is because `display` property of `<span>` is set to `inline` by default. _(For `<div>` is set to `block`)_

We can add and set `display` to a third value, `inline-block` to make it inline, but also has block property.

```css
.box {
  display: inline-block;
}
```

Note: you can delete the space between 2 `<span>` to make 2 boxes adjacent to each other:

```html
<body>
  <span class="box"></span><span class="box"></span>
</body>
```

---

##### Overflowing

The `overflow` property specifies whether to clip the content or to add scrollbars when the content of an element is too big to fit in the specified area.

The overflow property has the following values:

- `visible` - Default. The overflow is not clipped. The content renders outside the element's box
- `hidden` - The overflow is clipped, and the rest of the content will be invisible
- `scroll` - The overflow is clipped, and a scrollbar is added to see the rest of the content
- `auto` - Similar to scroll, but it adds scrollbars only when necessary

Ex:

```css
.box {
  width: 200px;
  height: 200px;
  border: 3px solid gold;

  /* set overflow property to 'auto' */
  overflow: auto;
}
```

==Note: The overflow property only works for block elements with a specified height.==

==Note: In OS X Lion (on Mac), scrollbars are hidden by default and only shown when being used (even though "overflow:scroll" is set).==

---

##### Measurement units

CSS has several different units for expressing a length.

Many CSS properties take "length" values, such as `width`, `margin`, `padding`, `font-size`, etc.

Length is a number followed by a length unit, such as `10px`, `2em`, etc.

There are two types of measurement units: **absolute** and **relative**.

| Absolute |       |
| -------- | ----- |
| `px`     | Pixel |

| Relative |                                       |
| -------- | ------------------------------------- |
| `%`      | relative to the size of the container |
| `vw`     | relative to viewport _(view width)_   |
| `vh`     | relative to viewport _(view height)_  |
| `em`     | relative to font size                 |
| `rem`    | relative to font size                 |

==Note: The em and rem units are practical in creating perfectly scalable layout!==
==\* Viewport = the browser window size. If the viewport is 50cm wide, 1vw = 0.5cm.==

Ex:

```css
.box {
  /* 10 x font size of the current element */
  width: 15rem; /* based on font-size */
  height: 100vh; /* based on viewport */
  border: 3px solid gold; /* fixed size */
  background-color: lightblue;
}
```

---

##### Positioning

The position property specifies the type of positioning method used for an element (`relative`, `fixed` or `absolute`).

**position: relative;**

An element with `position: relative;` is positioned relative to its normal position.

Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

For example:

Say we have 3 `<div class="box">` boxes inside a big box `<div class="boxes">`

```html
<body>
  <div class="boxes">
    <!-- Make 2 classes for each, separate by space -->
    <div class="box box-one"></div>
    <div class="box box-two"></div>
    <div class="box box-three"></div>
  </div>
</body>
```

Color your boxes and set the second box to relative position:

```css
.boxes {
  border: 3px solid lightgrey;
}

.box {
  width: 5rem;
  height: 5rem;
}

.box-one {
  background-color: gold;
}

.box-two {
  background-color: tomato;
  /* box-two is relative to its normal position  */
  position: relative;

  left: 4rem;
  bottom: 2rem;

  /* Make box-two underneath the other boxes */
  z-index: -1;
}

.box-three {
  background-color: dodgerblue;
}
```

Note: The `z-index` property specifies the stack order of an element. _(the higher `z-index`, the higher the stack order)_

**position: absolute;**

An element with `position: absolute;` is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

==Note1: Absolute positioned elements are removed from the normal flow, and can overlap elements.==

Note2: When you set an `absolute` postion, its parent has to be `relative`.

For example:

```css
.boxes {
  border: 3px solid lightgrey;
  /* Set parent box to relative */
  position: relative;
}

.box {
  width: 5rem;
  height: 5rem;
}

.box-one {
  background-color: gold;
}

.box-two {
  background-color: tomato;
  /* set to absolute */
  position: absolute;
  right: 0;
  bottom: 0;
}

.box-three {
  background-color: dodgerblue;
}
```

In the case above, `box-two` will be display on another layer other than `box-one` and `box-three`. Hence, `box-one` and `box-three` won't save the space for `box-two` as it is in different universe~ (if you know multiverse lol)

**position: fixed;**

An element with `position: fixed;` is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.

For instance, if you want to stick your nav bar to the top as you scroll down the page, you can set `position: fixed;`

Ex:

```css
body {
  margin: 10px;
  height: 200vh; /* make a page longer to scroll */
}

.box-two {
  background-color: tomato;
  position: fixed;
  top: 0; /* make it stick to the top of the viewport */
  z-index: 10;
}
```

If you want to make your box wider:

```css
.box-two {
  background-color: tomato;
  position: fixed;
  top: 0;

  /* box starting from 2rem away from the left to 2rem away from the right */
  left: 2rem;
  right: 2rem;

  /* let browser decide width instead of parent */
  width: auto;
  z-index: 10;
}
```

---

##### Floating elements

The `float` property specifies whether an element should float to the left, right, or not at all.

Ex: Say you have a tweet with an avatar on the left, and text on the right:

```html
<body>
  <article class="tweet">
    <!-- Image  -->
    <div class="avatar"></div>
    <p>
      <!-- tweet Text... -->
    </p>
    <p class="clear">
      <!-- comment, like, share Text... -->
    </p>
  </article>
</body>
```

```css
.avatar {
  width: 5rem;
  height: 5rem;
  background-color: gold;

  /* set the avator float to the left */
  float: left;

  /* set a margin between image and text */
  margin-right: 1rem;
}
```

Note: Elements next to a floating element will flow around it. To avoid this, use the `clear` property.

```css
.clear {
  clear: both;
}
```

Another problem is when we have short text (shorter than avator) inside the `.tweet` class, the border will not include the avator, to avoid this, we need to `clear` again at the end of parent class, i.e. `.tweet`

We can either add another `<div class="clear">` at the end:

```html
<body>
  <div class="avatar"></div>
  <!-- ... -->
  <div class="clear"></div>
</body>
```

Or add pseudo element `::after` in css:

```css
/* replace '.tweet' with '.clearfix' and include multiple cases */
.tweet::after {
  content: "";
  display: block;
  clear: both;
}
```

---

##### Flexbox

The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.

To start using the Flexbox model, you need to first define a flex container.

Ex:

```html
<body>
  <div class="container">
    <div class="box">A</div>
    <div class="box">B</div>
    <div class="box">C</div>
  </div>
</body>
```

The flex container becomes flexible by setting the `display` property to `flex`:

The `flex-direction` property defines in which direction the container wants to stack the flex items. By default, it is set to `row`, you can set it to `column`, `column-reverse`, `row-reverse`

```css
.container {
  border: 3px solid lightgray;
  display: flex;
  /* flex item horizontally */
  flex-direction: row;
}
```

**Aligning items**

The `align-items` property is used to align the flex items.

- `justify-content` (along the **main** axis)
  - `center`, `flex-start`, `flex-end`, `stretch`, `baseline`, `space-evenly`, `space-between` etc
- `align-items` (along the **cross** axis)
- `align-content`
- `align-self`

```css
.container {
  /* position all item to the center of main axis, i.e. horizontal */
  justify-content: center;
  /* push all item to the end of cross axis, i.e. vertical */
  align-items: flex-end;
  /* Make the box longer so it can show the vertical axis */
  height: 90vh;
}
```

If we have too many boxes to fit in a single line, we can set `flex-wrap` property to `wrap`, and set `align-content` property to adjust the alignment:

```css
.container {
  /* Wrap all boxes and push em to the center */
  flex-wrap: wrap;
  align-content: center;
}

.box-one {
  /* only align box-one to the bottom and the rest stay at the center */
  align-self: flex-end;
}
```

**Sizing items**

- `flex-basis` (the initial size of a flex item)
- `flex-grow` (the growth factor)
- `flex-shrink` (the shrink factor)
- `flex` (shorthand for )

Note: all above should apply to flex items (i.e. `box`) instead of flex container (i.e. `container`)

**flex-basis**

The `flex-basis` property specifies the initial length of a flex item.

Ex:

```css
.box {
  /* the size of the box is 10x5 (width x height) */

  flex-basis: 10rem; /* 10rem will overwrite width if 'flex-direction' is row */
  width: 5rem;
  height: 5rem;
}
```

**flex-grow**

The `flex-grow` property specifies how much a flex item will grow relative to the rest of the flex items.

The value must be a number, default value is 0.

Ex:

```css
.box {
  flex-grow: 1;
}

.box-one {
  /* box-one grow faster than the other boxes */
  flex-grow: 2;
}
```

**flex-shrink**

The `flex-shrink` property specifies how much a flex item will shrink relative to the rest of the flex items.

```css
.box {
  flex-shrink: 1;
}
```

**flex**

The `flex` property is a shorthand property for the `flex-grow`, `flex-shrink`, and `flex-basis` properties.

```css
.box {
  /* flex-grow: 1 */
  flex: 1;
  /* flex-grow: 1; flex-basis: 15rem */
  flex: 1 15rem;
  /* flex-grow: 1; flex-shrink: 1 ;flex-basis: 15rem */
  flex: 1 1 15rem;
}
```

==Note: The value of `flex-grow` and `flex-shrink` has no units !==

---

##### Grid

The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.

To set an element to `grid`, first to set `display` property to `grid`, then set the size of the grid.

```css
.container {
  display: grid;

  /* 3 x 2 */
  grid-template-rows: repeat(3, 100px); /* equal to "100px 100px 100px" */
  grid-template-columns: repeat(2, 100px);

  /* easier way to set rows and cols at a time */
  grid-template: repeat(3, 100px) / repeat(2, 100px);

  border: 3px solid grey;
}
```

**Aligning items**

Similar to flex
The `align-items` property is used to align the items.

==Note: by default, they are set to `stretch`==

Move an item inside the container

- `justify-items` (along the **horizontal** axis) e.g. `left`, `right`, `center`.
- `align-items` (along the **vertical** axis)

Move the grid as a whole

- `justify-content`
- `align-content`

**fr Unit**

`fr` stands for fraction, which is another unit when it comes to creating grid.

By using `fr` , we are telling CSS to use a number of fraction of the available space in the container.

```css
.container {
  display: grid;

  /* Row: 100px fixed 1st& 3rd row, 2nd will be resized when you change the browser size. */
  /* Col: 30% for 1st col, 70% for 2nd col */
  grid-template: 100px auto 100px / 30fr 70fr;
}
```

**Gap**

Gaps between each row and column

- `row-gap`
- `column-gap`
- `gap` (shorthand for row&col-gap)

Ex:

```css
.container {
  row-gap: 10px;
  column-gap: 10px;

  /* row-gap: 10px, col-gap: 10px */
  gap: 10px;

  /* row-gap: 10px, col-gap: 20px */
  gap: 10px 20px;
}
```

**Placing items** (Item properties)

- `grid-row`
- `grid-column`
- `grid-area`

Ex:
Say we want the first box (header) to span the entire top row, we must need `grid-row` to place the box.

```css
.box-one {
  /* span column from col 1 to col 3 */
  grid-column: 1 / 3;
  /* Alternatively, use '-1` to represent the last col */
  grid-column: 1 / -1;
  /* Alternatively, use `span 2` to indicate span the next 2 cols */
  grid-column: 1 / span 2;

  /* place the box starting at row 2, ending before row 4 */
  grid-row: 2 / 4;

  /* start / end */
  /* row / column */
  grid-area: 1 / 1 / 1 / 3;
}
```

**Placing items in named areas** (Item properties)

You can also define a name for each block and use `grid-area` to indicate the area each box should go to.

- `grid-template-areas`
- `grid-area`

To started with, define names of the grid in the container using `grid-template-areas`:

```css
.container {
  /* define area's name separated by space */
  grid-template-areas:
    "header header" /* row 1 col 1 & row 1 col 2: header */
    "sidebar main" /* row 2 col 1: sidebar,  row 2 col 2: main */
    ". footer"; /* row 3 col 1: . row 3 col 2: footer */
}
```

Next, call the name of the block to place each item: (without `""`)

```css
.box-one {
  grid-area: header;
}
.box-four {
  grid-area: footer;
}
```

---

##### Hiding elements

Hiding elements is simple, say we have 2 `<p>`

```html
<body>
  <p class="first">First</p>
  <p>Second</p>
</body>
```

- `display` specifies how an element should be displayed

- `visibility` specifies whether or not an element should be visible

Ex:

```css
.first {
  /* not to display the text */
  display: none;
  /* hide the text, but save the space */
  visibility: hidden;
}
```

---

##### Media queries

The `@media` rule is used in media queries to apply different styles for different media types/devices.

In other words, media queries allows us to change the layout when the user switch from one platform to another.

Ex: say we have 2 boxes of text, we want to display them vertically in mobile and horizontally on desktop.

```html
<body>
  <div class="container">
    <!-- box 1 -->
    <div class="box">
      <p>
        <!-- dummy text -->
      </p>
    </div>
    <!-- box 2 -->
    <div class="box">
      <p>
        <!-- dummy text -->
      </p>
    </div>
  </div>
</body>
```

To start off with, we develop mobile view first since it is smaller and easier to design:

```css
.container {
  display: flex;
  /* set the boxes to display vertically */
  flex-direction: column;
}

.box {
  /* set the box color */
  background-color: gold;
  padding: 1rem;
}

/* target the second element of the box */
.box:nth-of-type(2) {
  background-color: dodgerblue;
}
```

The issue is that the current boxes are aligned vertically, it is easier to read, but when the screen size gets wider, it is difficult to read each line.

Hence, we need a breakpoint to change the box align horizontally using `@media`

```css
/* If it is displayed on a screen, whose size is between 600px and 900px  */
@media screen and (min-width: 600px) and (max-width: 900px) {
  .container {
    /* change boxes to display horizontally */
    flex-direction: row;
  }
}

/* If it is printed, make sure font-size use 'pt' unit to look formal as well as 'cm' as padding  */
@media print {
  body {
    font-size: 12pt;
  }

  .box {
    padding: 0.5cm;
  }
}
```

In sum, we use media queries to apply some certain rules only when some certain conditions are met.

---

##### Summary of Layout

- When rendering an HTML document, the browser puts each element inside a box. The
  box contains four areas: the content area, the padding area, the border area and the
  margin area.
- Padding is the space between the border and the content area. Margin is the space
  outside of an element and should be used to separate elements from each other.
- Margin collapsing happens when the top and bottom margins of elements are
  combined into a single margin. The size of the margin is equal to the largest of the two
  margins.
- There are two types of HTML elements: block-level and inline.
- Block-level elements always start on a new line and take up the entire available
  horizontal space. The `<p>` and `<div>` elements are examples of block-level elements.
- Inline elements don’t start on a new line. They take up as much width as necessary. The
  `<span>`, `<a>` and `<img>` are a few examples of inline elements.
- We can size elements by setting their width and height properties. These properties
  have no effect on inline elements. To size an inline element, we need to set its `display`
  property to `inline-block`.
- By default, the width and height properties are applied to the content box. So paddings
  and borders increase the size of the visible box. This behavior can be changed by setting
  the `box-sizing` property to `border-box`.
- Overflow occurs when an element’s content is too large to fit. Using the `overflow`
  property we can specify what should happen when overflow occurs.
- Measurement units in CSS fall into two categories: absolute and relative units. Examples
  of absolute units are px, pt, in, cm, etc. Examples of relative units are %, vw, vh, em and
  rem.
- Using the position property we can precisely position an element. The default value
  of this property is `static`. If we change the value of this property, the element is considered positioned.
- By setting the `position` to `relative`, we can position an element relative to its
  normal position. By setting it to `absolute`, we can position it relative to its positioned
  parent. That means, the parent (or ancestor) should be a positioned element. By setting
  the position to `fixed`, we can position the element relative to the viewport.
- By setting the `float` property, we can push an element to the left or right side of its
  container. Other elements will flow around the floated element and fill the available
  space.
- Floated elements are invisible to their parent. This behavior is called collapsing parent
  and often causes layout issues. To fix this, we have to clear the floated elements.
- The Flexible Box Layout (or FlexBox or just Flex) is used for laying out elements in one
  direction (in a row or column). A common application of Flex is in building navigation
  menus.
- The Grid Layout is a two-dimensional grid system. It’s often used to lay out major page
  areas, photo galleries, etc.
- With media queries we can provide different styles for different devices depending on
  their features such as screen size, orientation, etc. The most common application of
  media queries is in providing different styles based on the viewport width.
- By using media queries and relative measurement units we can build responsive web
  sites that adjust smoothly to various screen sizes.

---

#### Typography

Typography is the art of creating beautiful and easy-to-read text. Given that 95% of the
content on the web is text, as a front-end developer, you must ensure that the text on
your web pages is easy to read and visually appealing on various screen sizes.

---

##### Styling fonts

Fonts fall into three main categories: Serif, Sans-serif and Monospace. Serif fonts have a
line/stroke at the edges of their characters. They’re more professional and serious.
Sans-serif fonts don’t have those edges. They’re more modern, warm and friendly.
Monospace fonts have equal-width characters. They’re often used in displaying code.

```css
body {
  margin: 10px;
  /* ctrl + space to check font stack */
  font-family: Georgia, "Times New Roman", Times, serif;
}

p {
  /* 100-900, normal, bold, light... */
  font-weight: normal;
  font-style: italic;
  font-size: 1rem;
  color: #333;
}
```

---

#### Transformations, Transitions, and Animations

---

#### Writing Clean, Maintainable CSS

---

### Keyboard shortcut for Mac

`shift + option + down` to duplicate block of code

`shift + up/down` to select multiple lines of code

`option + up/down` to move selected code up/down

`cmd + d` to show 2 cursors to replace a name with 2 selected variable

**Zen Coding:**
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
