# Landing Page Maintenance Guide

This guide will help you maintain and customize the Muggengaas Voor Campers landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold text-gray-800">MuggenGaas</a>
```
Simply replace "MuggenGaas" with your desired text.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Kenmerken</a>
    <!-- Additional menu items -->
</div>
```
Replace "Kenmerken" and other menu text while keeping the classes intact.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">Muggengaas Voor Campers</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Geniet van zorgeloze nachten...</p>
```
- Update the h1 text while maintaining the responsive sizing classes
- Modify the paragraph text as needed

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow">
    <h3 class="text-xl font-semibold mb-4">Duurzaam Materiaal</h3>
    <p class="text-gray-600">Hoogwaardig muggengaas dat...</p>
</div>
```
To modify:
1. Change the h3 text for the feature title
2. Update the paragraph text for the description
3. Keep all Tailwind classes to maintain styling

## Managing Links

### Navigation Links
Current internal links are:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates section IDs on the page
2. Ensure section IDs match these href values
3. For external links, replace with full URLs

### Call-to-Action Buttons
Located in hero and final sections:
```html
<a href="https://amzn.to/4cuEuxa" class="inline-block bg-blue-600 text-white...">
```
Replace the Amazon link with your desired URL while keeping all classes.

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors">Over Ons</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors">Algemene Voorwaarden</a></li>
</ul>
```
Replace `#` with actual page URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Files
1. Create `privacy.html` and `terms.html` in your project folder
2. Copy the basic structure from `index.html`
3. Update the title and content accordingly

### Step 2: Update Footer Links
```html
<!-- Replace these placeholder links -->
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors">Algemene Voorwaarden</a></li>
```

### Step 3: Maintain Consistent Styling
- Copy the header and footer from index.html to new pages
- Keep all Tailwind CSS classes consistent
- Update the active state in navigation if needed

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout**
   - Check that all Tailwind classes remain intact
   - Verify container divs aren't accidentally deleted
   - Ensure responsive classes (md:, lg:) are preserved

2. **Missing Styles**
   - Confirm the Tailwind CDN link is present:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   - Verify the Inter font link remains in the head section

3. **Navigation Issues**
   - Check that section IDs match navigation href values
   - Ensure smooth scroll class remains on html tag:
   ```html
   <html lang="nl" class="scroll-smooth">
   ```

### Need Help?
- Double-check all closing tags
- Use browser inspector tools to identify styling issues
- Keep original file as backup before making changes
- Test all links after updates

Remember to test the page across different screen sizes after making any changes to ensure responsive design remains intact.