# Introduction

HTML (HyperText Markup Language) is the fundamental building block of the web. It provides the structure and content for web pages, defining elements like headings, paragraphs, links, images, and more.

# Key Components

## 1. Tags

Tags are the basic building blocks of HTML. They define the structure and meaning of content.

- **Opening Tag**: Starts with `<` followed by the tag name (e.g., `<p>`, `<h1>`, `<div>`)
- **Closing Tag**: Starts with `</` followed by the tag name (e.g., `</p>`, `</h1>`, `</div>`)
- **Content**: The text or other HTML elements placed between the opening and closing tags

## 2. Attributes

Attributes provide additional information about HTML elements.

- **Purpose**: Modify element behavior or appearance (e.g., `class`, `id`, `style`, `src`)
- **Format**: `attribute="value"` (e.g., `class="my-class"`, `src="image.jpg"`)
- **Placement**: Always placed inside the opening tag

## 3. Elements

An HTML element consists of:
- Opening tag
- Content (optional)
- Closing tag (for most elements)

**Note**: Some elements are "void" or "self-closing" and don't have closing tags (e.g., `<br>`, `<img>`, `<input>`, `<meta>`, `<link>`).

## 4. DOCTYPE Declaration

- The `<!DOCTYPE html>` declaration must be placed at the very beginning of the HTML document
- It tells the browser that this document uses HTML5
- It ensures the browser renders the page in standards mode

## 5. Nesting

HTML elements can be nested within other elements, creating a hierarchical structure called the DOM tree.

- Elements must be properly nested (closed in reverse order of opening)
- Example: A `<p>` element can be nested inside a `<div>` element

# Basic HTML Template

```html
<!DOCTYPE html>
<html lang="en"> 
  <head>
    <meta charset="utf-8" />
    <title>My First Webpage</title>
    <link rel="stylesheet" href="css/styles.css" />
  </head>
  <body>
    <h1>This is a Heading</h1>
    <p class="intro">This is a paragraph with a class attribute.</p>
    <img src="image.jpg" alt="An image">
    <script src="js/scripts.js"></script>
  </body>
</html>
```

## Understanding the Template

### Document Structure

- **`<!DOCTYPE html>`**: Declares this as an HTML5 document
- **`<html lang="en">`**: The root element with language attribute
  - `lang="en"` specifies the document language (important for accessibility and SEO)
  - [Valid language codes reference](https://www.w3schools.com/tags/ref_language_codes.asp)

### Head Section

The `<head>` contains metadata and resources:

- **`<meta charset="utf-8">`**: Defines character encoding
  - UTF-8 supports all languages and special characters
  - Must be the first element in `<head>`
  - [Learn more about character sets](https://www.w3schools.com/html/html_charset.asp)
  
- **`<title>`**: Sets the browser tab title and SEO page title

- **`<link>`**: Links external resources (self-closing)
  - Commonly used for CSS stylesheets
  - Typically placed in the `<head>` section

### Body Section

The `<body>` contains all visible content:

- **`<h1>`**: Main heading (use only one per page for SEO)
- **`<p>`**: Paragraph with a class attribute for styling
- **`<img>`**: Self-closing image element with required `alt` attribute
- **`<script>`**: Links JavaScript files
  - Usually placed at the end of `<body>` for better performance
  - Allows DOM to load before script execution

# Common HTML Elements

## Text Elements

- **Headings**: `<h1>` to `<h6>` (hierarchical importance)
- **Paragraph**: `<p>`
- **Line break**: `<br>` (self-closing)
- **Horizontal rule**: `<hr>` (self-closing)
- **Strong/Bold**: `<strong>` (semantic) or `<b>` (visual)
- **Emphasis/Italic**: `<em>` (semantic) or `<i>` (visual)

## Structural Elements (HTML5)

- **`<header>`**: Page or section header
- **`<nav>`**: Navigation links
- **`<main>`**: Main content (one per page)
- **`<section>`**: Thematic grouping
- **`<article>`**: Self-contained content
- **`<aside>`**: Sidebar or related content
- **`<footer>`**: Page or section footer

## Lists

- **Unordered list**: `<ul>` with `<li>` items
- **Ordered list**: `<ol>` with `<li>` items
- **Description list**: `<dl>` with `<dt>` (term) and `<dd>` (description)

## Links and Media

- **Anchor/Link**: `<a href="url">text</a>`
- **Image**: `<img src="url" alt="description">`
- **Video**: `<video>` with source elements
- **Audio**: `<audio>` with source elements

## Forms

- **Form container**: `<form>`
- **Input fields**: `<input>` (various types)
- **Text area**: `<textarea>`
- **Select dropdown**: `<select>` with `<option>` elements
- **Button**: `<button>` or `<input type="button">`

# Best Practices

1. **Semantic HTML**: Use elements for their meaning, not appearance
2. **Accessibility**: Always include `alt` attributes for images
3. **Valid HTML**: Close all tags properly and nest correctly
4. **Performance**: Place scripts at the end of body
5. **SEO**: Use proper heading hierarchy and meta tags

# Reference Links

- [MDN HTML Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [Structuring Content with HTML](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content)
- [HTML5 Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)