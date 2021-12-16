# **Introduction to Web Dev :D**

## Front End Journey 101 Memos

---

## Table of Content

- [Introduction] (#Introduction)

---

### _Introduction_

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

### _HTML basics_

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

### _HTML Tags_

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
  - `alt=` what to display if the image fails to display (_alternative_)

---

### _CSS basics_

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

### _Development tools_

If you encounter some issues with your HTML or CSS that your web page doesn't display the expected tag/style. It is difficult to _Debug_ your code since HTML & CSS doesn't mark up your bugs like other programming language. (╥﹏╥)

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
