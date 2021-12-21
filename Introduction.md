# **Introduction to Web Dev**

Front End Journey 101 Memos

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

  - [CSS basics](#css-basics)
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

Relative URL is a simply way to link to a different html page or element.

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

Relative URL sometimes is messy especially when we have multiple levels of folder, we can use absolute URL to solve this issue by starting with a `/` before the name.

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

---

#### Containers

---

#### Semantic Elements

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
