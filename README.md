# AV Accounting Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the AV Accounting landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Modifying Text Content

The landing page is divided into several key sections. Here's how to update text in each:

#### Header Section
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-blue-600">AV Accounting</a>
```
To change the company name, simply modify the text between the `<a>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Ascot Vale accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Accounting excellence with a personal touch
</p>
```
- Update the main heading by changing the text within the `<h1>` tags
- Modify the subheading by editing the text within the `<p>` tags

### Understanding Tailwind CSS Classes

Key classes used in this template:

1. **Responsive Design Classes**
   - `md:` prefix: Applies styles on medium screens (768px+)
   - `lg:` prefix: Applies styles on large screens (1024px+)
   Example:
   ```html
   <div class="text-xl md:text-2xl">
   ```
   This makes text larger on medium screens.

2. **Spacing Classes**
   - `px-4`: Horizontal padding of 1rem
   - `py-24`: Vertical padding of 6rem
   - `mb-6`: Bottom margin of 1.5rem

3. **Color Classes**
   - `text-blue-600`: Blue text
   - `bg-white`: White background
   - `hover:bg-blue-700`: Darker blue on hover

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update these:
1. Locate the section you want to link to
2. Add an `id` attribute to that section if missing
3. Update the `href` attribute to match the `id`

### External Links
The main call-to-action button currently points to:
```html
<a href="https://theaccountants.com">
```

To update:
1. Replace `theaccountants.com` with your actual domain
2. Ensure the URL includes `https://`
3. Test the link after updating

## Linking Privacy and Terms Pages

### Adding Policy Pages to Footer
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive
   ```html
   <!-- Correct -->
   <section id="services">
   <a href="#services">
   
   <!-- Wrong -->
   <section id="Services">
   <a href="#services">
   ```

2. **Responsive Design Issues**
   - Check that you're maintaining responsive classes when editing
   - Keep both mobile and desktop classes:
   ```html
   <!-- Correct -->
   <h1 class="text-4xl md:text-5xl lg:text-6xl">
   
   <!-- Wrong (removed responsive classes) -->
   <h1 class="text-4xl">
   ```

3. **Color Consistency**
   - Main brand color is blue-600
   - When adding new elements, use:
     - `text-blue-600` for text
     - `bg-blue-600` for backgrounds
     - `hover:bg-blue-700` for hover states

### Need Help?
- Double-check all changes against the original HTML
- Test on multiple screen sizes
- Verify all links work before deploying
- Keep a backup of the original file

Remember to test all changes in a development environment before pushing to production.