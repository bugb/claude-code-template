# HTML Learning Module - Claude Instructions

This file contains specific instructions for working with HTML learning materials in this directory.

## Project Structure

```
frontend/core/html/
├── README.md              # Main HTML lecture content
├── CLAUDE.md             # This file - HTML-specific instructions
└── demos/                # Interactive HTML demonstrations
    ├── index.html        # Demo navigation hub
    ├── semantic-elements.html
    ├── forms.html
    ├── media.html
    ├── demo-styles.css   # Shared demo styles
    └── [future demos]
```

## HTML Demo Standards

### Required Features for ALL HTML Demos
1. **CSS Toggle Button**: Every demo MUST include the eye-catching CSS toggle functionality
   - Gradient background (blue for ON, red for OFF)
   - Pulsing glow animation
   - Emoji indicators (🎨 for CSS ON, 📄 for CSS OFF)
   - Fixed position (top: 20px, right: 20px)
   - Proper JavaScript toggle function

2. **Navigation**: Include back link to demo index
3. **Semantic HTML**: Use proper HTML5 semantic elements
4. **Educational Value**: Include explanations and code examples
5. **Responsive Design**: Work on all screen sizes

### CSS Toggle Button Code Template
```html
<!-- In <style> section -->
<style id="demo-styles">
  /* CSS Toggle Button - Eye-catching Design */
  .css-toggle {
    position: fixed;
    top: 20px;
    right: 20px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 12px 20px;
    border: 3px solid #ffffff;
    border-radius: 50px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    z-index: 1000;
    transition: all 0.3s ease;
    box-shadow: 0 8px 25px rgba(102, 126, 234, 0.4);
    text-transform: uppercase;
    letter-spacing: 1px;
    animation: pulseGlow 2s infinite;
  }
  /* [Additional CSS styles...] */
</style>

<!-- In <body> -->
<button class="css-toggle" onclick="toggleCSS()">CSS: ON</button>

<!-- JavaScript function -->
<script>
function toggleCSS() {
  const styleElement = document.getElementById('demo-styles');
  const toggleButton = document.querySelector('.css-toggle');
  
  if (styleElement.disabled) {
    styleElement.disabled = false;
    toggleButton.textContent = 'CSS: ON';
    toggleButton.classList.remove('css-disabled');
  } else {
    styleElement.disabled = true;
    toggleButton.textContent = 'CSS: OFF';
    toggleButton.classList.add('css-disabled');
  }
}
</script>
```

## Content Guidelines

### README.md Structure
1. **Introduction** with interactive demo links
2. **Key Components** (detailed explanations)
3. **Common HTML Elements** (organized by category)
4. **Best Practices** (comprehensive guide)
5. **Reference Links** (authoritative sources)

### Writing Style
- Use clear, beginner-friendly language
- Include practical examples for every concept
- Provide code snippets with explanations
- Use emojis sparingly for visual appeal
- Follow markdown best practices

### Code Examples
- Always use proper HTML5 syntax
- Include semantic elements where appropriate
- Follow naming conventions (lowercase, descriptive)
- Show both basic and advanced usage
- Validate all HTML examples

## Demo Creation Process

When creating new HTML demos:

1. **Plan the demo**: Define learning objectives
2. **Create HTML structure**: Use semantic elements
3. **Add educational content**: Explanations and examples
4. **Style appropriately**: Make it visually appealing
5. **Implement CSS toggle**: Use the standard template
6. **Test functionality**: Ensure toggle works properly
7. **Add to index**: Update demos/index.html navigation
8. **Update README**: Add demo link if significant

## Maintenance Guidelines

### When updating existing demos:
- Preserve the CSS toggle functionality
- Maintain consistent styling across demos
- Update index.html if demo titles/descriptions change
- Test all links and functionality

### When adding new concepts:
- First add to README.md lecture content
- Create demo if concept benefits from visualization
- Follow the established demo structure
- Update demo index navigation

## Educational Philosophy

### Focus on Vanilla HTML
- Emphasize semantic meaning over visual appearance
- Teach proper HTML structure first
- Use CSS toggle to show HTML without styling
- Explain accessibility and SEO benefits

### Progressive Learning
- Start with basic concepts
- Build complexity gradually
- Provide multiple examples per concept
- Include real-world use cases

### Interactive Learning
- Encourage hands-on exploration
- Provide editable examples where possible
- Use visual demonstrations effectively
- Include "try it yourself" suggestions

## Quality Standards

### All HTML content must:
- Be semantically correct
- Follow accessibility best practices
- Include proper alt text for images
- Use appropriate heading hierarchy
- Validate against HTML5 standards
- Work across modern browsers

### All demos must:
- Load without external dependencies (except demo-styles.css)
- Include the standardized CSS toggle button
- Have consistent navigation and styling
- Be mobile-responsive
- Include educational explanations

## Commit Guidelines

When working on HTML content, use these commit prefixes:
- `feat(html):` - New HTML features or demos
- `docs(html):` - Updates to HTML lecture content
- `fix(html):` - Bug fixes in HTML demos or content
- `style(html):` - CSS/styling updates for HTML demos
- `refactor(html):` - Code improvements without feature changes

## Future Enhancements

Planned improvements for the HTML module:
- Additional demos for tables, lists, text formatting
- Interactive exercises with form validation
- HTML5 API demonstrations (if applicable)
- Accessibility testing tools integration
- Performance optimization examples