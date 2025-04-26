# Knuffels Kleurplaat Landing Page - Maintenance Guide

This guide will help you maintain and customize the Knuffels Kleurplaat landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo text:

```html
<header class="fixed w-full bg-gray-900/95 backdrop-blur-sm z-50 border-b border-gray-800">
    <nav class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
            <a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
                Knuffels Kleurplaat  <!-- Change logo text here -->
            </a>
```

To modify:
1. Find the text "Knuffels Kleurplaat"
2. Replace it with your desired logo text
3. Adjust text size by changing `text-2xl` to larger (`text-3xl`) or smaller (`text-xl`)

### Hero Section
The main headline and call-to-action section:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent animate-fade-in">
    Koop Knuffels Kleurplaat Met Korting  <!-- Change main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    🔥 Nog maar enkele exemplaren beschikbaar!  <!-- Change subheadline here -->
    <span class="font-semibold text-purple-400">Bestel nu met speciale korting</span>
</p>
```

To modify:
1. Update the headline text between the `<h1>` tags
2. Change the subheadline text in the `<p>` tag
3. Adjust text size using Tailwind classes:
   - Desktop: `lg:text-7xl`
   - Tablet: `md:text-6xl`
   - Mobile: `text-4xl`

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-800 rounded-xl p-8 hover:scale-105 transition duration-300 border border-gray-700">
    <div class="text-purple-400 text-4xl mb-4">⭐</div>  <!-- Change emoji here -->
    <h3 class="text-xl font-bold mb-4">Exclusief Design</h3>  <!-- Change title here -->
    <p class="text-gray-400">Unieke kleurplaten die nergens anders te vinden zijn!</p>  <!-- Change description here -->
</div>
```

To add/modify features:
1. Copy the entire `<div>` block above
2. Change the emoji, title, and description text
3. Paste within the `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8` container

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external links, use the full URL: `https://example.com`
4. Update the link text between `<a>` tags

### Call-to-Action Links
The main CTA buttons use this format:

```html
<a href="https://amzn.to/3GoxZQw" class="inline-block bg-gradient-to-r from-purple-600 to-pink-600 text-white font-bold py-4 px-8 rounded-full text-lg hover:scale-105 transform transition duration-300 shadow-lg hover:shadow-purple-500/25">
    Bekijk Aanbieding
</a>
```

To update:
1. Replace `https://amzn.to/3GoxZQw` with your desired URL
2. Change the button text ("Bekijk Aanbieding")
3. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Link Setup
Current footer links:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to policy pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check that all Tailwind CSS classes are spelled correctly
   - Verify that closing tags match opening tags
   - Ensure the Tailwind CDN link is working

2. **Non-Working Links**
   - Verify that section IDs match the href attributes
   - Check for typos in URLs
   - Ensure file paths are correct for local files

3. **Responsive Issues**
   - Look for `md:` and `lg:` prefixes in classes
   - Test at different screen sizes
   - Verify that the viewport meta tag is present

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Use browser developer tools to inspect elements

Remember to always test your changes across different devices and browsers before publishing updates to your live site.