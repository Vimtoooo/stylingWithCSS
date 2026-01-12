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
