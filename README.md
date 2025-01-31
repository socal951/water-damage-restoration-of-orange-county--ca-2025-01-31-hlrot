# Water Damage OC Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Water Damage OC landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

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
<div class="text-blue-600 font-bold text-xl">
    Water Damage OC  <!-- Update this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Update menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
Located at the top of the page, featuring main headline and description:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Water Damage Restoration of Orange County, Ca  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Restoring Peace to Your Home...  <!-- Update description -->
</p>
```

### Tailwind CSS Tips for Beginners
- Text sizes use classes like `text-xl`, `text-2xl`, etc. (larger number = bigger text)
- Colors use format `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing uses `m` (margin) or `p` (padding) with numbers in multiples of 4 (e.g., `mb-8` = margin-bottom 2rem)
- Responsive classes start with screen sizes: `md:` or `lg:`

## Managing Links

### Internal Navigation Links
These links scroll to page sections:

```html
<!-- Update these href attributes to match your section IDs -->
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <!-- Replace # with your actual social media URLs -->
    <a href="#" class="hover:text-white transition-colors duration-300">
        <i class="fab fa-facebook"></i>
    </a>
    <a href="#" class="hover:text-white transition-colors duration-300">
        <i class="fab fa-twitter"></i>
    </a>
</div>
```

### Contact Information
Update email and website in the footer:

```html
<div class="space-y-4">
    <h4 class="text-lg font-semibold text-white">Contact</h4>
    <p>Email: socalwaterdamage@gmail.com</p>  <!-- Update email -->
    <p>Website: waterdamagerestorationoc.com</p>  <!-- Update website -->
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Add Links to Footer
Insert these links in the Quick Links section:

```html
<div class="space-y-4">
    <h4 class="text-lg font-semibold text-white">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in the same directory as `index.html`
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your privacy policy and terms content between them

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify responsive classes (md:, lg:) are properly set
   - Test all screen sizes

3. **Icon Display Problems**
   - Confirm Font Awesome CDN is loaded
   - Check icon class names against Font Awesome documentation
   - Example: `fa-facebook` should be `fab fa-facebook`

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using Chrome DevTools (F12)
- Check browser console (F12) for JavaScript errors

Remember to always test changes in multiple browsers and screen sizes before deploying to production.