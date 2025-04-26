# Landing Page Maintenance Guide

Welcome to the maintenance guide for the Ayla Doeken landing page. This document will help you make common updates and modifications to the page, even if you're new to web development.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and brand name. To update:

1. **Brand Name:**
```html
<a href="#" class="text-2xl font-bold text-gray-800">Ayla Doeken</a>
```
Simply replace "Ayla Doeken" with your desired brand name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Voordelen</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Kenmerken</a>
    <!-- Additional menu items -->
</div>
```
Replace the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Koop Ayla Doeken Met Korting
</h1>
```
- To modify heading size:
  - `text-4xl`: Default size
  - `md:text-5xl`: Size on medium screens
  - `lg:text-6xl`: Size on large screens

### Understanding Tailwind Classes
Common classes used in this page:
- `container`: Centers content
- `mx-auto`: Centers horizontally
- `px-4`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `text-gray-600`: Sets text color
- `bg-white`: Sets background color

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Kenmerken</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change the `href` value to match your section ID
2. Update the displayed text between the tags

### Call-to-Action Buttons
Current product link:
```html
<a href="https://amzn.to/44FEZmc" class="inline-block bg-blue-600">
    Bekijk Aanbieding
</a>
```
Replace `https://amzn.to/44FEZmc` with your product URL.

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white">
        <!-- Facebook icon -->
    </a>
    <a href="#" class="hover:text-white">
        <!-- Instagram icon -->
    </a>
</div>
```
Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate this section in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white">Terms & Conditions</a></li>
</ul>
```

### Step 2: Add Proper Links
Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white">Terms & Conditions</a></li>
```

### Step 3: Create New Pages
1. Create `privacy.html` and `terms.html` in the same folder as `index.html`
2. Copy the header and footer from index.html to maintain consistent styling
3. Add your policy content between the header and footer

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Ensure section IDs match the href values
   - Example: `href="#features"` needs a matching `id="features"` in the page

2. **Responsive Design Issues**
   - Check Tailwind breakpoint classes:
     - `md:`: Medium screens (768px+)
     - `lg:`: Large screens (1024px+)
   - Test the page at different screen sizes

3. **Missing Styles**
   - Verify the Tailwind CSS link is correct:
   ```html
   <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
   ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test all links before publishing changes

Remember to always make a backup of your files before making significant changes!