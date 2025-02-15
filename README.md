# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "TWD":
```html
<div class="text-2xl font-bold text-gray-800">TWD</div>
```

2. **Navigation Menu Items**: Locate these lines to modify menu text:
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
<a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
```

### Hero Section
To update the main headline and subheading:

```html
<h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```

- `text-4xl`: Controls text size on mobile
- `md:text-6xl`: Controls text size on desktop
- `mb-6`: Adds margin bottom spacing

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <i class="fas fa-server text-4xl text-blue-600 mb-6"></i>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Professional hosting solution included with every website package.</p>
</div>
```

To modify:
1. Change icon: Update `fa-server` to any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update heading: Modify text in `<h3>` tag
3. Update description: Change text in `<p>` tag

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Internal links (same page): Use `#section-id`
2. External links: Use full URL
   ```html
   <a href="https://example.com">Example</a>
   ```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition duration-300"><i class="fab fa-facebook"></i></a>
    <a href="#" class="hover:text-white transition duration-300"><i class="fab fa-twitter"></i></a>
    <a href="#" class="hover:text-white transition duration-300"><i class="fab fa-linkedin"></i></a>
</div>
```

Replace `#` with your social media profile URLs:
```html
<a href="https://facebook.com/yourpage" class="hover:text-white transition duration-300">
```

## Linking Privacy and Terms Pages

### Current Footer Legal Section
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### To Add Privacy and Terms Links:
1. Create privacy.html and terms.html in your website folder
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Mobile classes come before desktop (md:) classes
   - Example: `class="text-sm md:text-lg"`
   - Test on different screen sizes

3. **Icons Not Showing**
   - Verify Font Awesome CSS is loaded
   - Check icon class names are correct
   - Use [Font Awesome documentation](https://fontawesome.com/icons) for reference

4. **Styling Problems**
   - Tailwind classes must be exact matches
   - Check for proper spacing between classes
   - Use browser inspector to verify class application

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Inspect elements using browser developer tools (F12)
- Test all links after making changes
- Verify changes on both mobile and desktop views

Remember to always backup your files before making changes, and test thoroughly after each modification.