# HTML

- [HTML](#html)
  - [1 Introduction](#1-introduction)
  - [2 Tag and Text](#2-tag-and-text)
  - [2 DOCTYPE Declaration](#2-doctype-declaration)
  - [3 Start with a Example](#3-start-with-a-example)
  - [4 Comment](#4-comment)
  - [5 Heading](#5-heading)
  - [6 Div](#6-div)
  - [7 Paragraph](#7-paragraph)
  - [8 Text Format](#8-text-format)
  - [9 Image](#9-image)
  - [10 Url](#10-url)
  - [11 Title](#11-title)
  - [12 Enumerate](#12-enumerate)
  - [13 Table](#13-table)
  - [14 Form](#14-form)

## 1 Introduction

HTML is a kind of *Markup Language* whose full name is **HyperText Markup Language**.
It should be noticed that HTML is not a compiling language, therefore it should only be used to description a web page.

## 2 Tag and Text

HTML could be simply divided into two hands in which there are tags and text.

- Tags are series of names to tell which kinds of stuff you are about putting into your web;
- Text are the words you are about putting into your web.

In HTML, tags are denoted by tag's name and the surrounding symbol `<` and `>`
Every element in HTML is consist of head tag and foot tag. For instance

```html
<div>element</div>
```

## 2 DOCTYPE Declaration

`<!DOCTYPE>` is used in the headmost part of the HTML file whose function is to declare which version of HTML you are creating.

In this tutorial, we only talk about HTML5, the latest release. And it should use

```html
<!DOCTYPE html>
```

Notice that the uppercase and lowercase are both OK.

## 3 Start with a Example

Look at the example given underneath.

```html
<!DOCTYPE html>
<html>

    <body>
        <p>这是第一个段落。</p>
    </body>

</html>
```

Firstly, the `<html>` tag tells the browser that where is the file's beginning and where is the ending.

Then, the `<body>` tag tells the browser the content in it need to be showed on the web page.

Finally, the `<p>` tag as well as amounts of other tag tells browser how to show the web page.

The three things are essential in most web page.

## 4 Comment

In HTML, we can comment our code like underneath

```html
<!-- This is comment -->
```

## 5 Heading

Heading is the essential part in our writing. HTML has six different levels of heading. They can be denoted by `<h1>` ~ `<h6>`. The smaller the number is, the bigger the number is.

```html
<h1>Heading 1</h1>
    <h2>Subheading 1</h2>
```

In addition, `<hr>` donates a horizontal line, which is ofen used following the heading.

```html
<h1>Heading 1</h1>
<hr>
<h1>Heading 2</h1>
<hr>
```

## 6 Div

The tag `<div>` means one row's content. For example

```html
<div>The first row.</div>
<div>The second row.</div>
```

The `div` is the most widely used block element. Another kind of element is inline element. These 

## 7 Paragraph

The tag `<p>` means paragraph. The difference between `<div>` and `<p>` is that the paragraph will generate a greater distance between two paragraphs. It is more usually used in writing.

```html
<p>The first paragraph.</p>
<p>The second paragraph.</p>
```

Another tag `<br>` means wrapping around. But it should be noticed that it must used in paragraph or one independent row. For example

```html
<p>The paragraph is too long, <br>so it need to be divided into two rows.</p>
```

## 8 Text Format

Browser can reinforce text into differnt format. We just need to tell which kind of format we want.

| Tag | Format |
| --- | --- |
| `b` and `strong` | Bold |
| `i` and `em` | Italic |
| `small` | Samll |
| `sub` | Subscript |
| `sup` | Superscript |
| `ins` | Insert |
| `del` | Delete |

For instance

```html
<b>NOTICE</b>: ...
```

To other format, please navigate [HTML Text Format(Chinese)](https://www.runoob.com/html/html-formatting.html)

## 9 Image

An appropriate picture can make our web page more attractive. To add picture in our page, firstly, we need prepare image file, and then use `<img>` tag to insert it. For instance

```html
<img src="url">
```

The `src` parameter is the picture's url address. Alternatively, we can set a piece of text to replace the picture when the web fail to load the picture by `alt` parameter. For instance

```html
<img src="url" alt="image">
```

We can also change the picture's size for what we want by setting the `width` or the `height` parameter. For instance

```html
<img src="url" alt="image" width="w" height="h">
```

## 10 Url

Its important to put external ulr in our web. Tag `<a>` is certainly to do this.
It has several parameters, and the most important is `href` which tells the url of the external web.

```html
<a href="url">This is a url</a>
```

Another important parameter is the `target`. To use the code like underneath, we can open the url in a new tab.

```html
<a href="url" target="_blank">This is a url</a>
```

Another important usage of `a` tag is the bookmark. We can insert a `id` parameter in somewhere of our page, and use the `id` in other place of the page to jump back to the id's place. For instance

```html
<a id='tips'>Tips</a>
<!-- in the same page -->
<a href="#tips">Jump to the tips</a>
<!-- in other page -->
<a href="url#tips">Jump to the tips</a>
```

In addition, a url also can be embedded in a image. For instance

```html
<a href="url"><img src="url"></a>
```

## 11 Title

The web title doesn't display on the page, but display on the tab or the **Favorites**.
We can set the title for whatever we want by `head` and `title` tag.

```html
<html>
<head>
    <title>Title</title>
</head>
<body></body>
</html>
```

To other important tags which can be used in `head`, please navigate [HTML Head(Chinese)](https://www.runoob.com/html/html-head.html)

## 12 Enumerate

One of powerful tools in writing is enumerate. In HTML, there is ordered enumerate `ol` and unordered enumerate `ul`. For instance

```html
<ul>
    <li>Coffee</li>
    <li>Milk</li>
</ul>

<ol>
    <li>Coffee</li>
    <li>Milk</li>
</ol>
```

## 13 Table

Table is useful when we put a lot of data in our web page. A table example can be used in HTML is put underneath

```html
    <table border="1">
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>
```

Some usual parameters in `table` tag is put in the underneath table

| Tag | Function |
| --- | --- |
| `table` | Define table |
| `th` | Define table's head |
| `tr` | Define table's row |
| `td` | Define table's data cell |
| `caption` | Define table's title |
| `colgroup` | Define table's column group |
| `col` | Define table's column's property |
| `thead` | Define table page's head |
| `tbody` | Define table's body |
| `tfoot` | Define table page's foot |

## 14 Form

Tag `form` is used to create a field for users to interaction. The most widely used element in `form` is `input`. For instance

```html
<form action="">
    Username: <input type="text" name="user"><br>
    Password: <input type="password" name="password">
</form>
```

The code will generate two text field with on to input *username* and another to input *password*.

There are lots of types to option for `input`. We can create a radio button like this

```html
<form action="">
    <input type="radio" name="sex" value="male">male<br>
    <input type="radio" name="sex" value="female">female
</form>
```

And create a checkbox like this

```html
<form>
    <input type="checkbox" name="vehicle" value="Bike">I love bycycle.<br>
    <input type="checkbox" name="vehicle" value="Car">I love cars.
</form>
```

We can submit what we input in `form` by a `submit` button. For instance

```html
<form name="input" action="html_form_action.php" method="get">
    Username: <input type="text" name="user"><input type="submit" value="Submit">
</form>
```

The `action` means what the server would do to the data you submit, and the `method` means the method the data submit to the server. Generately, it has two choice to choose, `get` and `post`.

You can navigate [Html Form(Chinese)](https://www.runoob.com/html/html-forms.html) for more element used in `form`.
