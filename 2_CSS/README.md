# CSS

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
