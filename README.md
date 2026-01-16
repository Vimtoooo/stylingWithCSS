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

![Inline CSS Result](images/Inline%20CSS.jpg)

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

![Internal CSS Example](images/Internal%20CSS.jpg)

### External CSS:

External CSS is a method of adding CSS styles to an HTML document by placing them in a **separate CSS fiel** and linking that file to the HTML document using the `<link>` tag. This approach allows you to apply the same styles to multiple HTML pages, making it easier to maintain and update the design of your website. 
External CSS is ideal for **large projects** where consistency and efficiency are crucial.

#### Basic Syntax and Example of Usage:

Here's how to use external CSS:

1. Create a CSS file (e.g. `styles.css`) with your CSS rules.

```css
body {
    background-color: lightblue;
}
p {
    color: blue;
    font-size: 16px;
}
```

2. Link the CSS file to your HTML document by adding a `<link>` tag in the `<head>` section:

```html
<!DOCTYPE html>
<html>
<head>
    <title>External CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Welcome to My Page</h1>
    <p>This is a paragraph of text.</p>
</body>
</html>
```

#### Breakdown:

In this example, the `<link>` tag connects the `styles.css` file to the HTML document. 

- `<head>`: A tag at the top of an HTML document that contains information about the page (e.g. title, links to CSS files, metadata and scripts), but all this information is **not shown on the webpage itself**.
- `<link>`: A self-closing tag that is located within the `<head>` tag, with the functionality of connecting external resources to your HTML file, such as a CSS file for styling.
- `rel`: This attribute specifies the relationship between the HTML document and the linked file (stylesheet).
- `href`: An attribute that specified the path to the CSS file (if it were to be in a folder, you would use `/` for the path, e.g. `stylesheets/styles.css`).

##### Result:

![External CSS](images/External%20CSS.jpg)

## Basic Selectors:

### Introduction to Selectors:

In CSS, selectors are patterns used to **select the HTML elements** that you would want to style. They are a crucial part of CSS rules, as they determine which elements the styles will be applied to. There are various types of selectors, each targeting elements in different ways. Understanding selectors is **fundamental to mastering CSS and creating well-styled web pages**.

#### Basic Syntax:

Here's a basic CSS rule with a selector:

```css
selector {
    property: value;
}
```

* `selector`: Targets the HTML elements to be styled.
* `property`: The style attribute you want to change (e.g. color, font-size).
* `value`: The value you want to set for the property (e.g. blue, 16px).

#### Example of Usage:

```css
p {
    color: blue;
    font-size: 16px;
}
```

In this example, `p` is the **selector**, targeting all paragraph elements. The declarations set the text color to blue and the ont size to 16 pixels for all paragraphs. 

### Type Selector:

The **type selector**, also known as the **element selector** or **tag selector**, targets HTML elements based on their tag names. It is one of the simplest and most fundamental selectors in CSS.

#### Basic Syntax:

```css
tagname {
    property: value;
}
```

* `tagname`: The name of the HTML tag you want to style (e.g. h1, div...).
* `property`: The CSS property you want to set (e.g. color, font-size).
* `value`: The value you want to set for the property (e.eg. blue, 16px).

#### Example of Usage:

```css
p {
    color: blue;
    font-size: 16px;
}
```

In the example above, the type selector `p` targets all `<p>` (paragraph) elements in the HTML document. The declarations set the text color to blue and the font size to 16 pixels for all paragraphs in the HTML file.

Let's say that we would want to include a diversity of styles, internally within our HTML document.

```html
<html>
<head>
    <title>Type Selector</title>
    <style>
        /* CSS rules are applied here! */
        h1 {
            color: darkred;
        }
        h2 {
            color: green;
        }
        p {
            color: blue;
            font-size: 18px;
        }
        div {
            background-color: lightblue;
        }
    </style>
</head>
<body>
    <h1>This is a main heading</h1>
    <h2>This is a subheading</h2>
    <p>This is a paragraph.</p>
    <div>This is a division.</div>
</body>
</html>
```

##### Result:

![Type Selectors](images/Type%20Selectors.jpg)

### Class Selectors:

The **class selector** is used to select HTML elements based on the **value of their `class` attribute**. It allows you to apply the same styles to multiple elements across your document. Class selectors are particularly useful when you want to **style a group of elements in the same way**, regardless of their tag names.

#### Basic Syntax:

To target elements with a specific class in your CSS, you use a period (`.`) followed by the class name. Here's the basic syntax for using a class selector.

```css
.classname {
    property: value;
}
```

> [!NOTE]
> Once the period has been placed, all classes of the same group will have the specified styles applied in your webpage!

#### Example of Usage:

```html
<html>
<head>
    <title>Class Selector</title>
    <style>
        /* Write CSS rules here */
        .blue-text {
            color: blue;
        }
        .large-text {
            font-size: 24px;
        }
    </style>
</head>
<body>
    <h1 class="blue-text">This is a main heading</h1>
    <h2 class="large-text">This is a subheading</h2>
    <p class="blue-text">This is a paragraph.</p>
    <p class="large-text">This is another paragraph.</p>
    <div>This is a division.</div>
</body>
</html>
```

##### Result:

![Class Selectors](images/Class%20Selectors.jpg)

#### Why should I use Class Selectors?

Not only that the class selectors allow you to group two or more element tags and apply the same styles, but to keep your styles more organized. For example:

- For highlighting -> `color: yellow` and `background-color: black`.
- For tables -> `color: purple`.
- For captions -> `font-size: 12px`.

But remember to mention the **`class` attribute** when groping styles together!

### ID Selector:

The **ID selector** is used to **target a specific HTML element** based on the value of its **`id` attribute**. Unlike class selectors, which can be used to style multiple elements, ID selectors are unique and can only be applied to a **single element on a page**. This makes them useful for styling **individual elements** with specific styles that should **not be applied to any other element**.

#### Basic Syntax:

To target an element with a specific ID in your CSS, you use a hash symbol (`#`) followed by the IS value. Here's the basic syntax for using an ID selector.

```css
#idname {
    property: value
}
```

#### Example of Usage:

```css
#intro {
    color: blue;
    font-size: 20px;
}
```

In this example, the ID selector `#intro` targets the element with the IS "intro". This declarations set the text color to blue and the font size to 20 pixels for this elements.

Here is another example:

```html
<html>
<head>
    <title>ID Selector</title>
    <style>
        /* Write CSS rules here */
        #special {
            background-color: yellow;
            color: red;
        }
    </style>
</head>
<body>
    <h1>This is a main heading</h1>
    <p>This is a paragraph.</p>
    <div id="special">This is a division.</div>
</body>
</html>
```

##### Result:

![ID Selector](images/ID%20Selector.jpg)

### Group Selectors:

The **group selector** is used to **select multiple HTML elements** and apply the **same styles** to all of them. This is particularly useful when you want to apply a common set of styles to different elements without having to write separate rules for each element. By grouping selectors, you can write more concise and efficient CSS code.

#### Basic Syntax:

To use a group selector, you list the selectors that you would want to group, separated by commas (`,`). Here's the basic syntax:

```css
selector1, selector2, selector3 {
    property: value;
}
```

#### Example of Usage:

This this example, let's say you want to apply the same text color and font size to all `<h1>`, `<h2>` and `<p>` elements. You can use a group selector like this:

```css
h1, h2, p {
    color: blue;
    font-size: 16px;
}
```

This group selector targets all mentioned elements, while declaring the text color to blue and the font size to 16 pixels.

#### Mixing Selectors:

You can group any type of selectors, including type selectors, class selectors and ID selectors.

```css
h1, .highlight, #intro {
    background-color: yellow;
}
```

#### Complete Example:

Now, take this complete example:

```html
<html>
<head>
    <title>Group Selectors</title>
    <style>
        /* Write CSS rules here */
        h1, h2 {
            color: red;
        }
        p, div {
            background-color: lightgray;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <h1>This is a main heading</h1>
    <h2>This is a subheading</h2>
    <p>This is a paragraph.</p>
    <div>This is a division.</div>
</body>
</html>
```

##### Result:

![Group Selectors](images/Group%20Selectors.jpg)

### Universal Selector:

The universal selector is a powerful selector in CSS that targets **every HTML element on a page**. It is represented by an asterisk (`*`). When it is utilized, the universal selector applies the specified styles to all elements, regardless of their type, class or ID. This can by useful for setting global styles or resetting default styles across the entire document.

#### Basic Syntax:

```css
* {
    property: value;
}
```

#### Example of Usage:

For this example, let's say that you want to set the default text color and font size for all elements on a page. Then you can use the universal selector like this:

```css
* {
    color: black;
    font-size: 14px;
}
```

Now, this second example alters all elements to pursue the same color (dark grey) and font size (16px):

```html
<html>
<head>
    <title>Universal Selector</title>
    <style>
        * {
            color: darkgrey;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <h1>This is a main heading</h1>
    <h2>This is a subheading</h2>
    <p>This is a paragraph.</p>
    <div>This is a division.</div>
</body>
</html>
```

##### Result:

![Universal Selector](images/Universal%20Selector.jpg)

### Recap - Basic Selectors:

Let's recap on what we discussed in this topic:

- **Type Selectors**: Apply any styles into a single element.
    ```css
    p {
        color: white;
    }
    ```
- **Class Selectors**: Organize a set of styles for elements with the same class attribute value.
    ```css
    .fancy {
        background-color: purple;
        color: pink;
    }
    ```
- **ID Selector**: Apply styles for elements with the same ID attribute value.
    ```css
    #title {
        font-size: 45px;
    }
    ```
- **Universal Selector**: Set a pre determined style to all present elements within an HTML document.
    ```css
    * {
        color: cyan;
        font-size: 16px;
    }
    ```

#### Example of a Webpage:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Selection Challenge</title>
    <style>
        /* Type Selector */
        p {
            color: blue;
            font-size: 16px;
        }

        /* Class Selector */
        .highlight {
            background-color: yellow;
        }

        /* ID Selector */
        #special {
            background-color: lightgrey;
            font-size: 20px;
        }

        /* ID Selector */
        h1, li {
            color: red;
        }
    </style>
</head>
<body>
    <h1>This is a main heading</h1>
    <h2 class="highlight">This is a subheading</h2>
    <p>This is a paragraph.</p>
    <p>This is another paragraph.</p>
    <div class="highlight">This is a division.</div>
    <ul id="special">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
</body>
</html>
```

##### Result:

![Recap on Selectors](images/Recap%20on%20Selectors.jpg)

## Text Fundamentals:

### Text Color:

In CSS, the `color` property is used to set the color of the text **inside an element**, you acn apply different color values to text to enhance the appearance of your webpage.

#### Example of Usage:

```css
h3 {
    color: purple;
}
```

### Font Family:

In CSS, the **font-family** property is used to specify the **typeface for text within an HTML element**. This property lets you list preferred fonts for your text. If the first font isn't available, the browser will use the next one in the list, ensuring a similar look.

#### Basic Syntax:

Here's the basic syntax for using the `font-family` property:

```css
selector {
    font-family: font1, font2, generic-family;
}
```
##### Breakdown:

* `font1, font2`: The preferred font family names, listed in order of preference. If `font1` is not available, the browser will try `font2`, and so on.
* `generic-family`: A generic font family name, such as `serif`, `sans-serif`, `monospace`, `cursive`, or `fantasy`. This serves as a fallback if none of the specified fonts are available. You can think of it like a default font that will always be available no matter what situation you face.

#### Important Guidelines:

When specifying font family names, it's important to follow these guidelines:

- If a font family contains whitespace, it should be enclosed in **quotation marks** (e.g. `"Times New Roman"`, `"Courier New"`).
- Multiple font family names should be separated by commas.
- It's good practice to include a generic font family as the last option in the list to ensure that a suitable fallback is used if none of the specified font are available.

#### Example of Usage:

```html
<html>
<head>
    <title>Font Family</title>
    <style>
        h1 {
            font-family: "Times New Roman", Times, serif;
        }

        p {
            font-family: Arial, Helvetica, sans-serif;
        }
    </style>
</head>
<body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

##### Result:

![Font Family](images/Font%20Family.jpg)