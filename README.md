# Styling with CSS

## Introduction:

### What is CSS?

CSS is a powerful and essential language for **styling web pages**, allowing you to create visually appealing and well-designed websites with ease. It will operate with HTML to construct any content and bring it to life, transforming plain text and elements into beautiful, engaging layouts. With CSS, you have the ability to control the appearance of every aspect of your website, from colors and fonts to spacing and positioning!

### CSS Syntax: 

Within CSS, the syntax refers to the **set of rules** that define how CSS code should be written, you can also apply the same concept in different languages like Python or Java. Understanding CSS syntax is essential for creating well-structured and functional stylesheets. A basic CSS rule consists of a **selector** and a **declarator block**.

#### Basic CSS Rules:

* **Selector**: Specifies the HTML element you want to style (e.g. a `<div>` or an `<img>` tag).
* **Declaration Block**: Contains one or more declarations enclosed in curly braces `{}`.
* **Declaration**: Consists of a property and a value, separated by a colon `:` (e.g. color:green;).
* **Property**: The style attribute you want to change (e.g. color, font-size).
* **Value**: The value you want to set for the property (e.g. blue, 15px).

#### Example of Rules being Applied:

For example:

```css
p {
    color: blue;
    font-size: 16px;
}
```

In this example, the `p` is the **selector**, targeting **all paragraph elements**. The **declaration block** contains two declarations: One setting the text color to blue and the other setting the font size to 15 pixels.

### CSS Comments:

**Comments** are notes within the code that **do not get executed**, they are just for making the code more readable, maintainable and other documentations.

In CSS, comments are written between `/*` and `*/` tags (similar to Java's comments), where anything placed inside these tags will be treated as a comment and will not affect the styling of the page.

#### Syntax:

```css
/* This is a comment */
p {
    color: blue; /* This sets the text color to blue */
}
```

### The `<head>` Tag:

In HTML, a `<head>` tag is a container for **metadata about the HTML document**. Metadata is data that describes the document but is not displayed on the page itself. The `<head>` element is placed between the `<html>` tag and the `<body>` tag.

#### Elements that the `<head>` can Include:

The `<head>` tag can include various elements, such as:

- `<title>`: Specifies the **title of the HTML document**, which is displayed in the browser's title bar or tab.
- `<style>`: Contains internal CSS styles for the document.
- `<link>`: Links to external resources, such as a CSS file(s).
- `<meta>`: Provides metadata about the document, such as character set, description and keywords.
- `<script>`: Embeds client-side scripts, such as JavaScript.

#### Example of the `<head>` being Applied:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
    <style>
        body {
            background-color: lightblue;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Page</h1>
    <p>This is a paragraph of text.</p>
</body>
</html>
```

In this example, the `<head>` tag contains the `<title>` of the page and some internal CSS styles. The title "My Web Page" will be displayed in the browser's title bar, and the background color of the body will be set to light blue.

You can go the extra mile and include more elements to be nested within the `<head>` tag!

#### Elements in the `<head>` Tag:

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comprehensive Head Example</title>
    <link rel="stylesheet" href="main.css">
    <style>
        /* Internal styles can go here */
    </style>
    <script src="script.js"></script>
</head>
```

##### Breakdown of the Elements:

* `<meta charset="UTF-8">`: Sets the character encoding for your website to UTF-8, ensuring that special characters, symbols and emojis from almost all language display correctly in teh browser instead of showing up as random glitches(e.g. ``).
* `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Configures the viewport for responsive design.
    - `width=device-width`: Tells the browser to set the width of the page to match the screen width of the device, like for a phone screen.
    - `initial-scale=1.0`: Sets the initial zoom level to 100% when the page loads.
    * Note that without this feature, mobile browsers will often zoom out to show the desktop version of the site, making any text tiny and hard to read.
* `<title>Comprehensive Head Example</title>`: Sets the title of the web page, making it visible by the tab, your bookmarks and it is also the headline used by search engines like Googles!
* `<link rel="stylesheet" href="main.css">`: Connects your HTML file to an external CSS file named **`main.css`**, allowing you to keep any styling rules separate from your HTML structure, which is the standard best practice.
*`<style> ... </style>`: A container for writing CSS rules directly inside the HTML file. This simple feature makes it handy for customizing small, page-specific styles though external files (like the `<link>` above) are usually preferred for larger projects and bigger websites.
* `<script src="script.js"></script>`: Links an external JavaScript file named **`script.js`**. The JavaScript file will add any type of interactivity for your site (like button clicks or animations), the `src` attribute tells the HTML where to find all the script file.

### The `<title>` Tag:

In HTML, the `<title>` tag is used to define the **title of the HTML document**, this title will be displayed in teh browser's title bar or in the page's tab. This `<title>` tag is placed within the `<head>` section of the HTML document.

#### Basic Syntax:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
    <style>
        body {
            background-color: lightblue;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Page</h1>
    <p>This is a paragraph of text.</p>
</body>
</html>
```

In the example, the `<title>` tag sets the title of the page to "My Web Page". When you open this HTML file, you will see "My Web Page" in the title bar or in the tab.

## Adding CSS:

### Inline CSS:

**Inline CSS** is a method of **adding CSS styles** directly to an HTML element using the `style` attribute. This approach allows you to apply unique styles to **individual elements** without the need for external or internal stylesheets. Inline styles are useful for making quick, specific style changes to a single element!

#### Basic Syntax:

Here's the basic syntax for using inline CSS:

```html
<element style="property: value;"></element>
```

* `<element>`: The HTML element you want to style.
* `style`: An attribute that contains the CSS declarations.
* `property`: The CSS property you want to set (e.g. color, font-size).
* `value`: The value you wnt to set foe the property (e.g. blue, 16px).

#### Example of Usage:

```html
<p style="color: blue; font-size: 16px;">This is a paragraph with inline styles.</p>
```

In this example, the paragraph element has inline styles that set the text color to blue and the font size to 16 pixels. These styles will only apply to this specific paragraph element (which is the **selector** for this instance).

##### Result:

[![Inline CSS Result](images/Inline%20CSS.jpg)]

### Internal CSS:

Internal CSS is a method of **adding CSS styles to an HTML document** by placing them within a `<style>` tag in the `<head>` section of the document. This approach allows you to apply a large variety of styles to distinct selectors and elements like `<p>`, `<h1>` tags and even the background color, all in a single page without the need for external stylesheets. Internal CSS is useful for styling a single document or making quick style changes.

#### Basic Syntax and Example of Usage:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Internal CSS</title>
    <style>
        body {
            background-color: lightblue;
        }
        p {
            color: blue;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Page</h1>
    <p>This is a paragraph of text.</p>
</body>
</html>
```

In this example, the `<style>` tag contains CSS rules that set the background color of the `<body>` to light blue, and the color of the `<p>` (paragraph) to blue, including a font size being set to **16 pixels**. These styles will apply to all elements within the HTML document (background will always be light blue and all `<p>` tags will be in blue with their corresponding font size).

##### Result:

[![Internal CSS Example](images/Internal%20CSS.jpg)]