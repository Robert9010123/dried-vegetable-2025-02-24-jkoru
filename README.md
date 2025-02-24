# VEGEXPORT Landing Page Maintenance Guide

This guide will help you maintain and customize the VEGEXPORT landing page. It's written for beginners and provides detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing Navigation Links](#fixing-navigation-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**: Locate this line in the header:
```html
<div class="text-2xl font-bold text-green-700">VEGEXPORT</div>
```
Simply replace "VEGEXPORT" with your desired brand name.

2. **Announcement Bar**: Find this section at the top:
```html
<div class="bg-green-600 text-white py-2 px-4 text-center text-sm">
    <p>Fast Worldwide Shipping (5 days delivery) 🌍</p>
</div>
```
Update the text between `<p>` tags to change the announcement.

### Hero Section
The main banner section contains three key elements:

```html
<div class="max-w-4xl mx-auto text-center text-white">
    <h1 class="text-4xl md:text-6xl font-bold mb-6">DRIED VEGETABLE</h1>
    <p class="text-xl md:text-2xl mb-8">DRIED/FRESH VEGETABLE</p>
    <a href="https://vegatableexport.com/checkout" class="inline-block bg-green-600...">Shop Now</a>
</div>
```

To modify:
- Change the main heading by updating text in `<h1>`
- Modify the subheading in the `<p>` tag
- Update the button text in the `<a>` tag

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, 4xl, etc.)
- `font-bold`: Makes text bold
- `mb-[size]`: Adds margin bottom (4, 6, 8, etc.)
- `bg-[color]-[shade]`: Sets background color (green-600, gray-50, etc.)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right

## Fixing Navigation Links

### Desktop Navigation Menu
Locate this section:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600 hover:text-green-600 transition-colors duration-300">Home</a>
    <a href="#" class="text-gray-600 hover:text-green-600 transition-colors duration-300">Products</a>
    <a href="#" class="text-gray-600 hover:text-green-600 transition-colors duration-300">About</a>
    <a href="#" class="text-gray-600 hover:text-green-600 transition-colors duration-300">Contact</a>
    <a href="https://vegatableexport.com/checkout" class="bg-green-600...">Buy Now</a>
</div>
```

To update links:
1. Replace `#` with your actual page URLs
2. Update the checkout link with your actual checkout page URL
3. Repeat the same updates in the mobile menu section

### Footer Links
Find the footer section and update these areas:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-green-400 transition-colors duration-300">About Us</a></li>
        <li><a href="#" class="hover:text-green-400 transition-colors duration-300">Products</a></li>
        <li><a href="#" class="hover:text-green-400 transition-colors duration-300">Blog</a></li>
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Policies</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-green-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-green-400 transition-colors duration-300">Terms of Service</a></li>
        <li><a href="#" class="hover:text-green-400 transition-colors duration-300">Shipping Policy</a></li>
    </ul>
</div>
```

Replace the `#` with:
```html
<li><a href="privacy.html" class="hover:text-green-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-green-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly
   - Verify file locations are correct

2. **Styling Problems**
   - Make sure Tailwind CSS CDN link is working
   - Check for missing or mistyped classes
   - Verify responsive classes (md:, lg:) are correct

3. **Mobile Menu Issues**
   - Ensure Alpine.js CDN is properly loaded
   - Check x-data attributes are properly set
   - Verify mobile menu toggle button functionality

For additional help:
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser dev tools
- Check console for JavaScript errors

Remember to always test changes across different devices and browsers before deploying to production.