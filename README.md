# Rockville Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Rockville Tempered Glass Showers landing page. Follow these step-by-step instructions to make common updates while preserving the page's design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<h1 class="text-2xl font-semibold">Rockville</h1>
```
- Replace "Rockville" with your company name
- Adjust text size using Tailwind classes:
  - `text-xl` (smaller)
  - `text-2xl` (current size)
  - `text-3xl` (larger)

### Hero Section
Located at the top of the page with the main headline:

```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Tempered glass showers - safe & stylish
</h2>
```
- Update the headline text while keeping the HTML tags
- The classes ensure responsive text sizing:
  - `text-4xl`: mobile devices
  - `md:text-5xl`: medium screens
  - `lg:text-6xl`: large screens

### Feature Cards
Located in the features section:

```html
<div class="p-8 rounded-xl bg-gray-50 hover:shadow-lg transition duration-300">
    <i class="icon ion-md-water text-4xl text-gray-900 mb-4"></i>
    <h4 class="text-xl font-semibold mb-4">Hydrophobic Coating</h4>
    <p class="text-gray-600">Advanced coating technology...</p>
</div>
```
To add new feature cards:
1. Copy the entire `<div>` block
2. Paste it within the grid container
3. Update the icon class (ion-md-*)
4. Modify the heading and description text

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update internal links:
1. Locate the section ID you want to link to (e.g., `id="features"`)
2. Use that ID in the href with a # prefix (e.g., `href="#features"`)

To add external links:
1. Replace the `href="#..."` with the full URL
2. Example: `href="https://www.example.com"`

### Call-to-Action Links
Current CTA button:

```html
<a href="http://www.customeuroglass.com" class="inline-flex items-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-gray-900 hover:bg-gray-800 transition transform hover:scale-105 duration-300">
    Get Started
</a>
```

To update:
1. Replace the href URL
2. Modify button text between the tags
3. Keep all classes to maintain styling

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the legal links section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Don't remove responsive classes (md:, lg:)
   - Keep the existing spacing classes (p-8, mb-4, etc.)
   - Test on multiple screen sizes

3. **Icon Display Problems**
   - Verify the Ionicons CDN link is present in the head
   - Check icon class names against the Ionicons documentation
   - Ensure internet connectivity for CDN access

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify changes in multiple browsers
- Use browser developer tools (F12) to inspect elements
- Test all links after making changes

Remember to always backup your files before making significant changes, and test thoroughly across different devices and browsers.