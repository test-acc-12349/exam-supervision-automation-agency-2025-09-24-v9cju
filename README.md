# ExamAuto Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the ExamAuto landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page consists of these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- Contact Section
- Footer

### Updating Text Content

#### Company Name
```html
<!-- Located in header and footer -->
<div class="text-2xl font-bold text-gray-800">ExamAuto</div>
```
To change the company name, modify the text between these div tags.

#### Hero Section Text
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Exam Supervision Automation Agency
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Automate Your Exam Team With Cutting-Edge Solutions
</p>
```
Update these text sections to change your main headline and subheading.

### Modifying Tailwind Classes

#### Understanding Responsive Classes
In this template, responsive classes use these prefixes:
- `md:` - Applied at medium screens (768px and up)
- `lg:` - Applied at large screens (1024px and up)

Example:
```html
text-4xl md:text-5xl lg:text-6xl
```
This means:
- Mobile (default): text-4xl (2.25rem)
- Tablet (md): text-5xl (3rem)
- Desktop (lg): text-6xl (3.75rem)

#### Common Tailwind Classes Used
- Text Colors: `text-gray-900`, `text-gray-600`, `text-white`
- Background Colors: `bg-white`, `bg-gray-50`, `bg-blue-600`
- Spacing: `px-6`, `py-4`, `mb-8`, `mt-12`
- Flex Layout: `flex`, `items-center`, `justify-between`

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Locate the `<nav>` section in the header
2. Change the `href` value to match your new section IDs
3. Update the text between the `<a>` tags

### External Links
Current external links that need review:
```html
<!-- Main CTA Button -->
<a href="https://examsrus.com" class="inline-block bg-blue-600...">
    Get Started Today
</a>

<!-- Contact Email -->
<a href="mailto:test@test.com" class="text-lg hover:underline">
    test@test.com
</a>
```

To update:
1. Replace `https://examsrus.com` with your actual website URL
2. Change `test@test.com` to your actual contact email

## Linking Privacy and Terms Pages

### Current Footer Links Structure
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - Check for typos in IDs and href attributes
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify Tailwind classes have proper responsive prefixes
   - Test at different screen sizes

3. **Style Inconsistencies**
   - Maintain consistent color classes throughout
   - Use the same spacing patterns (px-6, py-4, etc.)
   - Keep button styles consistent across sections

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to always backup your files before making significant changes, and test your modifications across different browsers and devices.