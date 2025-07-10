# Introduction

HTML (HyperText Markup Language) is the fundamental building block of the web. It provides the structure and content for web pages, defining elements like headings, paragraphs, links, images, and more.

## 🚀 Interactive Demos

Explore HTML concepts with hands-on examples:

- [**View All Interactive Demos →**](demos/index.html)
  - [Semantic Elements Demo](demos/semantic-elements.html) - See HTML5 semantic elements in action
  - [Forms & Inputs Demo](demos/forms.html) - Interactive form elements and validation
  - [Media Elements Demo](demos/media.html) - Images, audio, video, and more

> **Note**: To view these demos online, enable GitHub Pages in your repository settings.

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
  - Allows DOM to load before script execution (The DOM is fully loaded before the script runs, You don’t need DOMContentLoaded or defer to safely manipulate elements.)

# Common HTML Elements

## Text Elements

- **Headings**: `<h1>` to `<h6>` (hierarchical importance)
- **Paragraph**: `<p>`
- **Line break**: `<br>` (self-closing)
- **Horizontal rule**: `<hr>` (self-closing)
- **Strong/Bold**: `<strong>` (semantic) or `<b>` (visual)
- **Emphasis/Italic**: `<em>` (semantic) or `<i>` (visual)

## Structural Elements (HTML5)

### When to Use Each Semantic Element

#### `<header>`
- Use for introductory content (headings, logos, navigation)
- Can be used within sections, not just for the entire page
- Often contains `<h1>`-`<h6>`, `<nav>`, or publication date

#### `<nav>`
- Use for major navigation blocks
- Site-wide navigation, table of contents, or pagination
- No need to declare a role attribute (implied by the tag)

#### `<main>`
- The main content area of the document
- Use only once per page
- Should not include repeated content like headers or footers
- Replace generic `<div id="main">` with this semantic tag

#### `<section>`
- Use for thematic grouping of content
- Should typically contain a heading element
- More generic than `<article>`
- Good for chapters, tabbed content, or numbered sections

#### `<article>`
- Use for self-contained, stand-alone content
- Should make sense when distributed independently
- Examples: blog posts, news articles, user comments, product cards
- Can contain `<header>`, `<footer>`, and other `<section>` elements

#### `<aside>`
- Use for content tangentially related to main content
- Sidebars, pull quotes, advertisements, or related links
- Should be meaningful even if removed from main content

#### `<footer>`
- Use for footer content of a section or page
- Not limited to copyright information
- Can contain author info, related links, or metadata
- Can be used within `<article>` or `<section>` elements

### Figure and Caption Elements

#### `<figure>` and `<figcaption>`
- `<figure>` wraps self-contained content like images, diagrams, code snippets
- Does not contribute to document outline
- `<figcaption>` provides a caption or legend
- Place `<figcaption>` as first or last child of `<figure>`

Example:
```html
<figure>
  <img src="chart.png" alt="Sales chart for 2024">
  <figcaption>Figure 1: Annual sales showing 25% growth</figcaption>
</figure>
```

### Semantic Structure Example

```html
<body>
  <header>
    <h1>My Website</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
      </ul>
    </nav>
  </header>
  
  <main>
    <article>
      <header>
        <h2>Article Title</h2>
        <time datetime="2024-01-15">January 15, 2024</time>
      </header>
      
      <section>
        <h3>Introduction</h3>
        <p>Article introduction text...</p>
      </section>
      
      <section>
        <h3>Main Content</h3>
        <p>Main article content...</p>
        
        <figure>
          <img src="example.jpg" alt="Example image">
          <figcaption>An example illustration</figcaption>
        </figure>
      </section>
      
      <footer>
        <p>Written by John Doe</p>
      </footer>
    </article>
    
    <aside>
      <h3>Related Articles</h3>
      <ul>
        <li><a href="#">Related Article 1</a></li>
        <li><a href="#">Related Article 2</a></li>
      </ul>
    </aside>
  </main>
  
  <footer>
    <p>&copy; 2024 My Website. All rights reserved.</p>
  </footer>
</body>
```

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

## Core Principles

1. **Semantic HTML**: Use elements for their meaning, not appearance
2. **Accessibility**: Always include `alt` attributes for images
3. **Valid HTML**: Close all tags properly and nest correctly
4. **Performance**: Place scripts at the end of body
5. **SEO**: Use proper heading hierarchy and meta tags

## HTML5 Syntax Rules

### Document Structure
- Always start with `<!DOCTYPE html>` declaration
- Include language attribute: `<html lang="en">` or `<html lang="en-us">`
- Always use `<head>` and `<body>` tags (even though technically optional)
- Include viewport meta tag for responsive design: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

### Naming Conventions
- **Use lowercase** for all element names: `<section>`, not `<SECTION>`
- **Use lowercase** for attribute names: `class="header"`, not `CLASS="header"`
- **Always quote attribute values**: `class="my-class"`, not `class=my-class`
- **Use lowercase for file names**: `index.html`, not `Index.HTML`
- **Use `.html` file extension** (not `.htm`)

### Code Formatting
- **Indentation**: Use 2 spaces (or consistent tabs)
- **Line length**: Avoid lines longer than 80 characters
- **Blank lines**: Separate logical blocks for readability
- **Closing tags**: Close all elements, even optional ones (`</p>`, `</li>`)

Example of well-formatted HTML5:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Main Heading</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
      </ul>
    </nav>
  </header>
  
  <main>
    <article>
      <h2>Article Title</h2>
      <p>Content paragraph with proper formatting.</p>
    </article>
  </main>
  
  <footer>
    <p>&copy; 2025 Your Company</p>
  </footer>
  <script src="script.js"></script>
</body>
</html>
```

## Advanced Best Practices

### Metadata and SEO
- Place `<meta charset="UTF-8">` as early as possible in `<head>`
- Use descriptive, unique `<title>` tags (50-60 characters)
- Add meaningful meta descriptions
- Include Open Graph tags for social sharing

### Images and Media
- Always specify `width` and `height` attributes to prevent layout shift
- Use descriptive `alt` text for accessibility and SEO
- Provide fallback content for `<video>` and `<audio>` elements

### Links and Navigation
- Use descriptive link text (avoid "click here")
- Add `title` attributes for additional context when needed
- Use `rel="noopener"` for external links opening in new tabs

### Forms and Inputs
- Always associate labels with form controls
- Use appropriate input types (`email`, `tel`, `number`, etc.)
- Include proper validation attributes

### Comments and Documentation
- Use comments sparingly and only when necessary
- Keep comments concise and meaningful
- Remove commented-out code before production

### Validation
- Regularly validate HTML using [W3C Markup Validator](https://validator.w3.org/)
- Fix all errors and warnings
- Test across different browsers and devices

# Reference Links

- [MDN HTML Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [Structuring Content with HTML](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content)
- [HTML5 Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [HTML best practices by hail2u](https://github.com/hail2u/html-best-practices)
- [HTML tips](https://markodenic.com/html-tips/)