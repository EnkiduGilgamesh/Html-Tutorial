# CSS

- [CSS](#css)
  - [1 Introduce](#1-introduce)
  - [2 Selector](#2-selector)
    - [2.1 Class Selector](#21-class-selector)
    - [2.2 ID Selector](#22-id-selector)
    - [2.3 Generation and Group](#23-generation-and-group)
  - [3 Properties](#3-properties)
    - [3.1 Margin and Padding](#31-margin-and-padding)
    - [3.2 float](#32-float)
    - [3.3 border](#33-border)
    - [3.4 background](#34-background)
  - [4 Font](#4-font)
    - [4.1 Font Size](#41-font-size)
    - [4.2 Font Weight](#42-font-weight)
    - [4.3 Font Family](#43-font-family)
    - [4.4 Line Height](#44-line-height)
    - [4.5 Font Style](#45-font-style)
    - [4.6 Font Variant](#46-font-variant)
  - [5 Position](#5-position)
    - [5.1 Relative Position](#51-relative-position)
    - [5.2 Absolute Position](#52-absolute-position)
    - [5.3 Fixed Position](#53-fixed-position)
    - [5.4 Inherit Position](#54-inherit-position)
    - [6 Display](#6-display)
  - [7 Relative Unit](#7-relative-unit)

## 1 Introduce

*CSS* is used to append styles for *html* tags or elements.

One of the ways to append *CSS* to *html* is to write the code in `style` in `head` tag. For instance

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            div{width: 200px; 
                height: 200px;
                background: red;
            }
        </style>
    </head>
    <body>
        <div>Test</div>
    </body>
</html>
```

Another way is to write the content in a `.css` file, and quote it in the *html* file. For instance, we write the content in `style` above in *div.css*

```css
/* -- div.css -- */
div{width: 200px; 
    height: 200px;
    background: red;
}
```

And then we can quote this file like this

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <link rel = "stylesheet" type = "text/css" href="div.css">
    </head>
    <body>
        <div>Test</div>
    </body>
</html>
```

The last way is to use in a tag. For instance

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
    </head>
    <body>
        <div style = "width: 200px; 
                      height: 200px;
                      background: red;">
                      Test</div>
    </body>
</html>
```

Notice that if the three ways appear in a file in the same time. The **third way is given the highest priority** and the **second way is given the lowest**.

## 2 Selector

In *1 Introduce*, actually we have learned the **tag selector** which will set the style by the html tags. There are another two kinds of selector in CSS.

### 2.1 Class Selector

When we set a tag in html, we can give it a `class`, then we can set the style by classes, so all the tags with the same class will use this style. For instance

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .style_class{width: 200px; 
                height: 200px;
                background: red;
            }
        </style>
    </head>
    <body>
        <div class = 'style_class'>Test</div>
    </body>
</html>
```

### 2.2 ID Selector

Like class, we can set the style by IDs which we give to a tag when we call it. But the diference between class and ID is that ID is unique in a html file, that means only the latest tag with the ID will use the style we set for it. For instance

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            #style_ID{width: 200px; 
                height: 200px;
                background: red;
            }
        </style>
    </head>
    <body>
        <div id = 'style_ID'>Test</div>
    </body>
</html>
```

Finally, the three selector has different priority. Generally, the `ID` is the highest, and the tag is the lowest. For instance

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            div{width: 200px; 
                height: 200px;
                background: blue;
            }
            .style_class{width: 200px; 
                height: 200px;
                background: yellow;
            }
            #style_ID{width: 200px; 
                height: 200px;
                background: red;
            }
        </style>
    </head>
    <body>
        <div >Test</div>
        <div id = 'style_ID'>Test</div>
        <div class = 'style_class'>Test</div>
    </body>
</html>
```

### 2.3 Generation and Group

If a tag is embedded in several tags, we can select it by generation selector. For instance

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            div p{width: 200px; 
                height: 200px;
                background: red;
            }
        </style>
    </head>
    <body>
        <div>
            <p>Test</p>
        </div>
    </body>
</html>
```

This selector will select all the tags embedded in a div tag. We can also replace the tag with `class` or `id`. For instance

```html
<style>
    .class_style #id_style p{width: 200px; 
        height: 200px;
        background: red;
    }
</style>
```

We can select multiple tag with group selector. For instance

```html
<style>
    .class_style_1, .class_style_2{width: 200px; 
        height: 200px;
        background: red;
    }
</style>
```

In conclusion, the more accurate the selector is, the higher priority it has.

## 3 Properties

In *1 Introduce* we have learned there are several properties in `style` can control a tag's style. Now let's see more.

Notice that different kinds of elements have different properties. For example, we can define the width and height for a block element, but cannot fot an inline element.

### 3.1 Margin and Padding

Property `margin` in `style` is the external distance between a block's border and others.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            #style_ID{width: 200px; 
                height: 200px;
                background: red;
            }
            .Margin{
                margin-top: 10px;
                margin-right: 10px;
                margin-bottom: 10px;
                margin-left: 10px;
            }
        </style>
    </head>
    <body>
        <div id = 'style_ID' class='Margin'>Test</div>
    </body>
</html>
```

We can simply it like underneath

```html
<style>
    .Margin{
        margin: 10px 10px 10px 10px;
    }
</style>
```

The number of parameters ranges from 1 to 4. If the parameters' number is:

1. one, it means top, right, bottom, left distance are the same;
2. two, it respectively means top and bottom, left and right distance;
3. three, it respectively means top, left and right, bottom disance;
4. four, it respectively means top, right, bottom, left distance.

While `padding` is the internal distance between a block with its border. Its usag is similar to `margin`. For instance

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            #style_ID{width: 200px; 
                height: 200px;
                background: red;
            }
            .Padding{
                padding-top: 10px;
                padding-right: 10px;
                padding-bottom: 10px;
                padding-left: 10px;
            }
        </style>
    </head>
    <body>
        <div id = 'style_ID' class='Padding'>Test</div>
    </body>
</html>
```

In `html` the whole page has a default margin and padding. We can reset it 0 like this

```html
<style>
    html{
        margin: 0;
        padding: 0;
    }
</style>
```

Or use `*` to select all the element

```html
<style>
    *{
        margin: 0;
        padding: 0;
    }
</style>
```

### 3.2 float

A block element's width is defaultly defined 100% as wide as a web page. So a block element will be defaulty put under another block element. After we define the width of a block, there may be empty space in that line. Using the `float` property will make the block try to align in the same line firstly. There are two parameters, `left` and `right`, meaning align at the direction. For instance

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .style_class{width: 200px; 
                height: 200px;
                background: red;
                float: left;
            }
        </style>
    </head>
    <body>
        <div class = 'style_class'>Test</div>
    </body>
</html>
```

For inline element, such as `a`, `span` etc. **we cannnot set height and width for them**. The height and width for them vary with its environment.

### 3.3 border

Property `border` is used to set the element's border.

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .borderTem{
                border-width: 10px;
                border-style: solid;
                border-color: red;
            }
            .styleTem{
                height: 100px;
                width: 100px;
            }
        </style>
    </head>
    <body>
        <div class = 'styleTem borderTem'>Test</div>
    </body>
</html>
```

We can simplify it like this

```html
<style>
    .borderTem{
        border: 10px solid red;
    }
<style>
```

Or we can set border in different directions respectively. For example

```html
<style>
    .borderTem{
        border: 10px solid red;
        border-right-width: 20px;
        border-top-style: dashed;
        border-bottom-color: blue;
    }
    .borderTem2{
        border: 10px solid red;
        border-left: 20px dashed blue;
    }
<style>
```

### 3.4 background

We actually have used `background` to set an element's background's color. But it has more options.

We can set an element's background with an image like this

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .imageTem{
                height: 190px;
                width: 100px;
                background-image: url(1.jpg);
            }
        </style>
    </head>
    <body>
        <div class = 'imageTem'>Test</div>
    </body>
</html>
```

If the image's size is not suit the `div`'s size, we can reset the image's size like this

```html
<style>
.imageTem{
    width: 190px;
    height: 100px;
    background-image: url(1.jpg);
    background-size: 190px 100px;
}
</style>
```

If the image is smaller, the image will be defaultly repeatedly put in the `div`. We can change the behavior like this

```html
<style>
.imageTem{
    width: 1900px;
    height: 1000px;
    background-image: url(1.jpg);
    background-size: 190px 100px;
    background-repeat: no-repeat;
}
</style>
```

The parameter `repeat-x` means the image will repeat horizontally, while the parameter `repeat-y` means the image will repeat vertically.

We can also control the position the image appear in the `div`.

```html
<style>
.imageTem{
    width: 1900px;
    height: 1000px;
    background-image: url(1.jpg);
    background-size: 190px 100px;
    background-position: 200px 200px;
</style>
```

The property has tow parameter with the second one controlling the y axis and default being set `center`.

## 4 Font

Fonts are one of the essential elements in a web page.

### 4.1 Font Size

We can set font size like this

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .fontTem{
                font-size: 18px;
                color: red;
            }
        </style>
    </head>
    <body>
        <div>
            <p>
                This is text with default size and color.
            </p>
            <p class = 'fontTem'>
                This is text with specified size and color.
            </p>
        </div>
    </body>
</html>
```

Besides pixcel, we can use these words to control the font size

| | | | |
| --- | --- | --- | --- |
| `xx-small` | `x-small` | `small` | `medium` |
| `large` | `x-large` | `xx-large` | |

### 4.2 Font Weight

We can control font's weight like this

```html
<style>
    .fontTem{
        font-weight: 200;
    }
</style>
```

The value usually ranges from 100 - 1000, and can be also set by some words.

| | | |
| --- | --- | --- |
| `lighter` | `light` | `normal` |
| `bold` | `bolder` | |

### 4.3 Font Family

We can change the font family like this

```html
<style>
    .fontTem{
        font-family: "Microsoft Yahei";
    }
</style>
```

Notice that only the users having the font installed in their computer can see the font like you. We can set multiple font family in the same time so that if the front font is missing, the latter one will be used instead. For example

```html
<style>
    .fontTem{
        font-family: "Microsoft Yahei", "Times New Roman", "Arial";
    }
</style>
```

Notice that if chinese characters are used in `html`, it's better to add this command in `head`

```html
<head>
    <meta charset="utf-8">
</head>
```

By the way, we can navigate the fonts installed in our computer by the command in control panel

```bash
fc-list >> font.txt
```

TODO: embedded font

### 4.4 Line Height

TODO: line height

### 4.5 Font Style

Italic style is an important property for a font. We can use a font's italic style like this

```html
<style>
    .fontTem{
        font-style: italic;
    }
</style>
```

But not all fonts have italic style. Another way to make fonts oblique in force is like this

```html
<style>
    .fontTem{
        font-style: oblique;
    }
</style>
```

### 4.6 Font Variant

Font variant has a value which can make capital letter smaller. For example

```html
<style>
    .fontTem{
        font-variant: small-caps;
    }
</style>
```

Finally, we can write all the properties above simply like this

```html
<style>
    .fontTem{
        font: arial bold italic small-caps 20px/50px;
    }
</style>
```

The first number in `20px/50px` is the font size and the second is line height. And other properties has no strict order.

## 5 Position

For a web page, we can regard it as a flow consist of one element to another. Defaultly, elements are set position to try them best to fill the whole page. In *3.2 Float*, We have learned how to change the flow from vertical to horizontal. Now we will set one element's position as we want.

### 5.1 Relative Position

A block element's relative position is relative to **its original position**. For instance

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .divTem{
                height: 200px;
                width: 200px;
                float: left;
            }
            .positionTem{
                height: 200px;
                width: 200px;
                float: left;
                position: relative;
                top: 50px;
                left: 50px;
            }
        </style>
    </head>
    <body>
        <div class = 'positionTem'></div>
        <div class = 'divTem'></div>
    </body>
</html>
```

Notice that we can choose only one property from `top` and `bottom`, `left` and `right`.

### 5.2 Absolute Position

Absolute position is the position relative **the closest father element**. If all the father elements have no position set, it will be relative to the `html` element.

In addition, if a element has an absolute position, it will be popped out from the standard flow of the web page. In other words, it has no influence on all the elements after it when aligning. For instance

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .divTem{
                height: 200px;
                width: 200px;
                float: left;
            }
            .positionTem{
                height: 200px;
                width: 200px;
                background: red;
                float: left;
                position: absolute;
                top: 50px;
                left: 50px;
            }
        </style>
    </head>
    <body>
        <div class = 'positionTem'></div>
        <div class = 'divTem'></div>
    </body>
</html>
```

### 5.3 Fixed Position

A element with fixed position will hold it place in a page when slide down or up. The position is only relative to the page.

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .positionTem{
                height: 200px;
                width: 200px;
                position: fixed;
                background: red;
                float: left;
                top: 50px;
                left: 50px;
            }
        </style>
    </head>
    <body style="height = 1000px">
        <div class = 'positionTem'></div>
        <div class = 'divTem'></div>
    </body>
</html>
```

### 5.4 Inherit Position

We can inherit the father element' position like this

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .positionFatherTem{
                height: 200px;
                width: 200px;
                position: fixed;
                background: red;
                top: 0;
                left: 0;
            }
            .positionChildTem{
                height: 100px;
                width: 100px;
                position: inherit;
                background: green;
                top: 0;
                left: 200px;
            }
        </style>
    </head>
    <body style="height = 1000px">
        <div class = 'positionTem'></div>
        <div class = 'divTem'></div>
    </body>
</html>
```

### 6 Display

The property `display` can control the elemrnt whether to display on the page. For example

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .displayTem{
                height: 200px;
                width: 200px;
                background: red;
                float: left;
                display: none;
            }
            .divTem{
                height: 200px;
                width: 200px;
                background: blue;
                float: left;
            }
        </style>
    </head>
    <body>
        <div class = 'displayTem'></div>
        <div class = 'divTem'></div>
    </body>
</html>
```

Another function of `display` is that it can change inline elements into block elements and vice versa. For instance

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .displayBlockTem{
                height: 200px;
                width: 200px;
                background: red;
                display: block;
            }
            .displayInlineTem{
                height: 200px;
                width: 200px;
                background: blue;
                display: inline;
            }
        </style>
    </head>
    <body>
        <div class = 'displayInlineTem'>test</div>
        <span class = 'displayBlockTem'>test</span>
    </body>
</html>
```

The parameter `inline-block` will give the element the characteristics from both inline and block element.

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            .displayTem{
                height: 200px;
                width: 200px;
                background: red;
                float: left;
                display: inline-block;
            }
        </style>
    </head>
    <body>
        <div class = 'displayTem'>Test</div>
        <span class = 'displayTem'>Test</span>
    </body>
</html>
```

## 7 Relative Unit

In front, we have learned to use pixcel as our length unit which is an absolute unit. We can use `%` as a relative unit which means the element how much long as the closest father element. For instance

```html
<html>
    <head>
        <title>
            A test
        </title>
        <style>
            *{margin: 0; padding: 0;}
            body, html{height: 100%}
            .relativeTem{
                height: 50%;
                width: 50%;
                background: red;
            }
        </style>
    </head>
    <body>
        <div class = 'relativeTem'>
            <div class = 'relativeTem'>
            </div>
        </div>
    </body>
</html>
```
