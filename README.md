# VistaSocial Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the VistaSocial landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To modify:

1. **Company Name**
```html
<!-- Located in header section -->
<div class="text-2xl font-bold text-blue-600">VistaSocial</div>
```
Simply replace "VistaSocial" with your desired company name.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Located directly below the header:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Complete all-in-one solution for your online social presence
</h1>
```
- To modify the main headline, replace the text between `<h1>` tags
- For the subheading, update the text in the following `<p>` tag
- The button text can be changed in the `<a>` tag below

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <h3 class="text-xl font-semibold mb-4">AI-Powered Creativity</h3>
    <p class="text-gray-600">Generate engaging content automatically...</p>
</div>
```
To update:
1. Modify the text in `<h3>` for feature titles
2. Change the description in the `<p>` tag
3. Icons can be updated by modifying the SVG paths

### Tailwind CSS Classes Explained
Common classes used throughout:
- `container mx-auto px-6`: Centers content with padding
- `text-[size]`: Controls text size (xl, 2xl, etc.)
- `font-[weight]`: Controls text weight (bold, semibold)
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color
- `py-[size]`: Adds vertical padding
- `px-[size]`: Adds horizontal padding

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change the `href` value to match your section IDs
2. Ensure corresponding sections have matching `id` attributes
3. For external links, use complete URLs: `href="https://example.com"`

### Call-to-Action Buttons
Located in hero and features sections:
```html
<a href="#" class="inline-block bg-blue-600 text-white...">
    Transform Your Social Strategy →
</a>
```
Replace `#` with your desired URL.

### Footer Links
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Features</a></li>
    <!-- Additional links -->
</ul>
```
Update `href` attributes with appropriate URLs or section IDs.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all `href` values match your file names exactly
   - Verify that section IDs exist for internal links
   - Test all links after updating

2. **Styling Problems**
   - Ensure Tailwind CSS CDN link is present in the head section
   - Check for typos in class names
   - Maintain responsive classes (md:, lg:) when updating

3. **Layout Issues**
   - Keep the container class on parent elements
   - Maintain the grid structure in features and benefits sections
   - Preserve responsive classes when modifying layouts

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check that all HTML tags are properly closed
- Validate your HTML using [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different screen sizes using your browser's developer tools.