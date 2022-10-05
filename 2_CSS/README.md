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
