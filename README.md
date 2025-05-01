# WebLondon Landing Page - Maintenance Guide

This guide will help you maintain and customize the WebLondon landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "WebLondon" to your brand name:
```html
<a href="/" class="text-2xl font-bold text-blue-600">WebLondon</a>
```

2. **Navigation Links**: Located in the header's `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other navigation items -->
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Best Websites In London</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom Websites For Your Business</p>
```

### Tailwind CSS Class Guide
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-6`, `mb-12`)
- `py-[size]`: Adds padding top and bottom (e.g., `py-24`)
- `bg-[color]`: Sets background color (e.g., `bg-blue-600`)

To modify spacing or sizing:
1. Numbers in Tailwind classes represent size units
2. Larger numbers = more space/size
3. Example: Change `mb-6` to `mb-8` for more bottom margin

## Managing Links

### Internal Navigation Links
Current internal links use hash (#) navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Ensure the href matches the section ID
2. Example: `href="#features"` links to `<section id="features">`

### External Links
The template contains these external links that need updating:
```html
<!-- Call-to-action buttons -->
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>

<!-- Email contact -->
<a href="mailto:contact@example.com">contact@example.com</a>
```

To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Replace `contact@example.com` with your email address

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholder links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Styling Problems**
   - Keep the `transition-colors duration-300` classes on interactive elements
   - Maintain the `hover:` classes for proper interaction effects
   - Don't remove `container mx-auto` from section wrappers

### Need Help?
- Double-check your changes against the original code
- Use browser inspection tools to identify CSS issues
- Test all links after making changes
- Verify your page on multiple screen sizes

Remember to always backup your code before making changes, and test thoroughly after each modification.