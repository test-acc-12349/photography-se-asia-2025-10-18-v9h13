# Photography SE Asia Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining and customizing your Photography SE Asia landing page. This documentation covers text updates, link management, styling modifications, and best practices for keeping your site current and functional.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Common Customizations](#common-customizations)
7. [Troubleshooting Guide](#troubleshooting-guide)

---

## Quick Start Overview

### What You're Working With

This landing page uses three main technologies:

- **HTML**: The structure and content of your page (the text, buttons, sections)
- **Tailwind CSS**: A utility-first CSS framework that controls how everything looks (colors, spacing, sizes)
- **Font Awesome**: Icon library providing the camera icons, checkmarks, and other visual elements
- **Vanilla JavaScript**: Interactive features like mobile menu, accordions, and form handling

### File Structure You Should Have

```
your-project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy - you'll create this)
├── terms.html (terms of service - you'll create this)
└── README.md (this file)
```

### Before You Start

1. **Make a backup** of your original `index.html` file
2. **Use a text editor** like VS Code, Sublime Text, or even Notepad
3. **Save after each change** and refresh your browser to see updates
4. **Use Ctrl+F (Cmd+F on Mac)** to find and replace text quickly

---

## Updating Text Content

### Understanding the Page Structure

Your landing page is organized into clear sections. Here's where to find and update each section's text:

#### 1. **Announcement Bar** (Top of Page)

**Location**: Lines 245-247

**Current Text**:
```html
<div class="announcement-bar">
    <p>🚚 Free worldwide shipping on orders over $50. Fast delivery in 5 days!</p>
</div>
```

**How to Update**:
1. Find the text between `<p>` and `</p>`
2. Replace with your new announcement
3. You can keep the emoji or remove it

**Example**:
```html
<!-- Change from: -->
<p>🚚 Free worldwide shipping on orders over $50. Fast delivery in 5 days!</p>

<!-- Change to: -->
<p>🎉 New Year Sale: 20% off all LED lighting equipment!</p>
```

---

#### 2. **Header/Navigation** (Logo and Menu)

**Location**: Lines 249-270

**Current Logo Text**:
```html
<span class="text-xl font-bold text-gray-900">Photography SE Asia</span>
```

**How to Update**:
1. Replace `Photography SE Asia` with your company name
2. The `text-xl` class controls size, `font-bold` controls weight
3. Leave the classes as they are unless you want to change styling

**Example**:
```html
<!-- Change from: -->
<span class="text-xl font-bold text-gray-900">Photography SE Asia</span>

<!-- Change to: -->
<span class="text-xl font-bold text-gray-900">Pro Camera Gear</span>
```

**Navigation Menu Items** (Lines 256-260):

These are the links in the top menu. To update:

```html
<a href="#features" class="text-gray-700 hover:text-black transition-colors duration-300 font-medium">Features</a>
```

- The text between `>` and `</a>` is what displays
- The `href="#features"` points to which section it links to
- Don't change the `href` unless you're renaming sections

---

#### 3. **Hero Section** (Large Image with Text)

**Location**: Lines 300-315

**Main Heading**:
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-4 tracking-tight leading-tight">Photography SE Asia</h1>
```

**How to Update**:
1. Replace `Photography SE Asia` with your main headline
2. `text-4xl` = size on mobile, `md:text-6xl` = size on desktop
3. `text-white` = text color

**Example**:
```html
<!-- Change from: -->
<h1 class="text-4xl md:text-6xl font-bold text-white mb-4 tracking-tight leading-tight">Photography SE Asia</h1>

<!-- Change to: -->
<h1 class="text-4xl md:text-6xl font-bold text-white mb-4 tracking-tight leading-tight">Professional Photography Equipment</h1>
```

**Subheading** (Line 311):
```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed">Best Photography Kit In SE Asia</p>
```

**Example Update**:
```html
<!-- Change from: -->
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed">Best Photography Kit In SE Asia</p>

<!-- Change to: -->
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed">Premium Equipment for Every Photographer</p>
```

---

#### 4. **Features Section** (Three Cards with Icons)

**Location**: Lines 330-395

**Section Heading** (Lines 330-333):
```html
<h2 class="section-heading">Premium Photography Equipment</h2>
<p class="section-subheading">Everything you need for professional photography in Southeast Asia</p>
```

**How to Update**:
- Replace the text inside the tags
- Don't remove the class names (they control styling)

**Individual Feature Cards**:

Each card has three parts: **Icon**, **Title**, and **Description**

**Example - LED Lighting Card** (Lines 338-355):

```html
<div class="card-hover bg-white p-8 rounded-xl border border-gray-200 hover:border-gray-300 transition-colors duration-300">
    <div class="feature-icon">
        <i class="fas fa-lightbulb"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3">LED Lighting</h3>
    <p class="text-gray-600 leading-relaxed mb-4">Professional-grade LED lighting systems...</p>
    <ul class="space-y-2 text-sm text-gray-700">
        <li class="flex items-center"><i class="fas fa-check text-black mr-2"></i>Color temperature control</li>
        <li class="flex items-center"><i class="fas fa-check text-black mr-2"></i>Energy efficient</li>
        <li class="flex items-center"><i class="fas fa-check text-black mr-2"></i>Lightweight and portable</li>
    </ul>
</div>
```

**To Update This Card**:

1. **Change the title**: Replace `LED Lighting` with your feature name
2. **Change the description**: Replace the paragraph text
3. **Change the bullet points**: Replace each `<li>` item text
4. **Change the icon**: Replace `fas fa-lightbulb` with another Font Awesome icon

**Available Icons** (Common ones):
- `fas fa-lightbulb` = Light bulb
- `fas fa-video` = Camera/Video
- `fas fa-camera` = Camera
- `fas fa-star` = Star
- `fas fa-bolt` = Lightning
- `fas fa-cog` = Gear
- Find more at [fontawesome.com](https://fontawesome.com/search)

**Complete Example**:
```html
<!-- Change from: -->
<h3 class="text-2xl font-bold text-gray-900 mb-3">LED Lighting</h3>
<p class="text-gray-600 leading-relaxed mb-4">Professional-grade LED lighting systems designed for optimal color accuracy...</p>

<!-- Change to: -->
<h3 class="text-2xl font-bold text-gray-900 mb-3">Studio Lighting Kits</h3>
<p class="text-gray-600 leading-relaxed mb-4">Complete lighting solutions for every studio setup, from beginner to professional...</p>
```

---

#### 5. **Benefits Section** (Text with Images)

**Location**: Lines 406-530

**Section Title** (Lines 408-411):
```html
<h2 class="section-heading">Why Choose Us</h2>
<p class="section-subheading">Exceptional service and quality products delivered to your doorstep</p>
```

**First Benefit Block - "Free Delivery"** (Lines 416-438):

```html
<h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Free Delivery</h3>
<p class="text-lg text-gray-600 mb-6 leading-relaxed">We offer completely free shipping on all orders across Southeast Asia...</p>
<ul class="space-y-3 mb-8">
    <li class="flex items-start">
        <i class="fas fa-check text-black mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Free shipping on all orders</span>
    </li>
    <!-- More items... -->
</ul>
```

**How to Update**:
1. Change the `<h3>` title
2. Change the paragraph text
3. Update each bullet point by changing the text inside `<span>`

**Example**:
```html
<!-- Change from: -->
<h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Free Delivery</h3>

<!-- Change to: -->
<h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Express Shipping</h3>
```

---

#### 6. **FAQ Section** (Accordion)

**Location**: Lines 570-650

**Section Title** (Lines 572-575):
```html
<h2 class="section-heading">Frequently Asked Questions</h2>
<p class="section-subheading">Find answers to common questions about our products and services</p>
```

**Individual FAQ Item** (Example - Lines 582-590):

```html
<div class="accordion-item">
    <button class="accordion-button" onclick="toggleAccordion(this)">
        <span>What is your return policy?</span>
        <i class="fas fa-chevron-down transition-transform duration-300"></i>
    </button>
    <div class="accordion-content px-6 pb-4">
        <p class="text-gray-700 leading-relaxed">We offer a 100% Satisfaction Guarantee...</p>
    </div>
</div>
```

**How to Update**:
1. Change the question in the `<span>` tag
2. Change the answer in the `<p>` tag inside `accordion-content`
3. Don't remove the `onclick="toggleAccordion(this)"` - it makes it work

**Example**:
```html
<!-- Change from: -->
<span>What is your return policy?</span>
<!-- Change to: -->
<span>How do I track my order?</span>

<!-- And update the answer: -->
<p class="text-gray-700 leading-relaxed">You'll receive a tracking number via email...</p>
```

---

#### 7. **Testimonials Section** (Customer Reviews)

**Location**: Lines 670-730

**Section Title** (Lines 672-675):
```html
<h2 class="section-heading">What Our Customers Say</h2>
<p class="section-subheading">Real experiences from professional photographers across Southeast Asia</p>
```

**Individual Testimonial** (Example - Lines 682-703):

```html
<div class="testimonial-card fade-in">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-700 mb-4 leading-relaxed">"Photography SE Asia has been my go-to source..."</p>
    <div class="flex items-center">
        <div class="w-12 h-12 bg-gray-300 rounded-full mr-4 flex items-center justify-center">
            <i class="fas fa-user text-gray-600"></i>
        </div>
        <div>
            <p class="font-semibold text-gray-900">Marcus Chen</p>
            <p class="text-sm text-gray-600">Professional Photographer, Bangkok</p>
        </div>
    </div>
</div>
```

**How to Update**:
1. Change the quote text in the `<p>` tag
2. Change the customer name in `<p class="font-semibold text-gray-900">`
3. Change the title/location in `<p class="text-sm text-gray-600">`
4. To change star rating: remove or add `<i class="fas fa-star"></i>` (5 = 5 stars)

**Example**:
```html
<!-- Change from: -->
<p class="text-gray-700 mb-4 leading-relaxed">"Photography SE Asia has been my go-to source for professional equipment..."</p>
<p class="font-semibold text-gray-900">Marcus Chen</p>
<p class="text-sm text-gray-600">Professional Photographer, Bangkok</p>

<!-- Change to: -->
<p class="text-gray-700 mb-4 leading-relaxed">"Best prices and fastest delivery I've experienced!"</p>
<p class="font-semibold text-gray-900">Jennifer Smith</p>
<p class="text-sm text-gray-600">Wedding Photographer, Manila</p>
```

---

#### 8. **Contact Section** (Contact Info and Form)

**Location**: Lines 777-835

**Section Title** (Lines 779-782):
```html
<h2 class="section-heading">Get in Touch</h2>
<p class="section-subheading">Have questions? We're here to help. Contact us anytime.</p>
```

**Contact Information** (Lines 786-804):

```html
<div class="flex items-start">
    <i class="fas fa-envelope text-2xl text-black mr-4 mt-1 flex-shrink-0"></i>
    <div>
        <h3 class="font-semibold text-gray-900 mb-1">Email</h3>
        <a href="mailto:adminx@led.com" class="text-gray-700 hover:text-black transition-colors duration-300">adminx@led.com</a>
    </div>
</div>
```

**How to Update Email**:
1. Change `adminx@led.com` in the `href="mailto:adminx@led.com"` part
2. Change the displayed email text (the second `adminx@led.com`)

**Example**:
```html
<!-- Change from: -->
<a href="mailto:adminx@led.com" class="text-gray-700 hover:text-black transition-colors duration-300">adminx@led.com</a>

<!-- Change to: -->
<a href="mailto:support@yourcompany.com" class="text-gray-700 hover:text-black transition-colors duration-300">support@yourcompany.com</a>
```

**Business Hours** (Lines 806-812):
```html
<h3 class="font-semibold text-gray-900 mb-1">Business Hours</h3>
<p class="text-gray-700">Monday - Sunday: 9:00 AM - 6:00 PM (SGT)</p>
```

**Example Update**:
```html
<!-- Change from: -->
<p class="text-gray-700">Monday - Sunday: 9:00 AM - 6:00 PM (SGT)</p>

<!-- Change to: -->
<p class="text-gray-700">Monday - Friday: 8:00 AM - 5:00 PM EST</p>
```

---

#### 9. **Footer** (Bottom of Page)

**Location**: Lines 871-950

**Company Description** (Lines 876-881):
```html
<div>
    <div class="flex items-center space-x-2 mb-4">
        <i class="fas fa-camera text-2xl text-white"></i>
        <span class="text-xl font-bold text-white">Photography SE Asia</span>
    </div>
    <p class="text-gray-400 text-sm leading-relaxed">Your trusted source for premium photography equipment across Southeast Asia.</p>
</div>
```

**How to Update**:
1. Change the company name in `<span>`
2. Change the description in `<p>`

**Example**:
```html
<!-- Change from: -->
<span class="text-xl font-bold text-white">Photography SE Asia</span>
<p class="text-gray-400 text-sm leading-relaxed">Your trusted source for premium photography equipment across Southeast Asia.</p>

<!-- Change to: -->
<span class="text-xl font-bold text-white">Pro Photo Gear</span>
<p class="text-gray-400 text-sm leading-relaxed">Premium photography equipment for professionals and enthusiasts worldwide.</p>
```

**Copyright Year** (Line 931):
```html
<p class="text-gray-400 text-sm mb-4 md:mb-0">&copy; 2024 Photography SE Asia. All rights reserved.</p>
```

**How to Update**:
1. Change `2024` to current year
2. Change company name

**Example**:
```html
<!-- Change from: -->
&copy; 2024 Photography SE Asia. All rights reserved.

<!-- Change to: -->
&copy; 2024 Pro Photo Gear. All rights reserved.
```

---

### Quick Text Update Checklist

Use this checklist to ensure you've updated all necessary text:

- [ ] Announcement bar message
- [ ] Header/Logo company name
- [ ] Hero section heading
- [ ] Hero section subheading
- [ ] Features section title and description
- [ ] All three feature card titles and descriptions
- [ ] All benefit section titles and descriptions
- [ ] All FAQ questions and answers
- [ ] All testimonial quotes, names, and titles
- [ ] Contact section email address
- [ ] Contact section business hours
- [ ] Footer company name and description
- [ ] Footer copyright year

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS uses **utility classes** - short class names that control specific styling properties. Instead of writing custom CSS, you combine multiple small classes.

### Common Tailwind Classes Used in Your Landing Page

#### **Text Styling**

| Class | What it does | Example |
|-------|-------------|---------|
| `text-white` | White text color | `class="text-white"` |
| `text-gray-900` | Dark gray text | `class="text-gray-900"` |
| `text-gray-600` | Medium gray text | `class="text-gray-600"` |
| `text-xl` | Larger text size | `class="text-xl"` |
| `text-4xl` | Very large text | `class="text-4xl"` |
| `font-bold` | Bold text | `class="font-bold"` |
| `font-semibold` | Medium bold | `class="font-semibold"` |

#### **Colors**

Tailwind uses a color scale: `gray-50` (lightest) to `gray-900` (darkest)

```html
<!-- Light gray background -->
<div class="bg-gray-50">Light</div>

<!-- Dark gray background -->
<div class="bg-gray-900">Dark</div>

<!-- Black background -->
<div class="bg-black">Very Dark</div>

<!-- White background -->
<div class="bg-white">White</div>
```

#### **Spacing (Padding and Margins)**

| Class | What it does |
|-------|-------------|
| `p-4` | Padding on all sides |
| `px-4` | Horizontal padding (left & right) |
| `py-4` | Vertical padding (top & bottom) |
| `mb-4` | Margin below |
| `mt-4` | Margin above |
| `space-y-4` | Vertical space between items |

**Example**:
```html
<!-- Add more space inside a box -->
<div class="p-8">More padding</div>

<!-- Add more space below text -->
<p class="mb-6">Text with margin below</p>
```

#### **Sizing**

```html
<!-- Width classes -->
<div class="w-full">Full width</div>
<div class="w-1/2">Half width</div>
<div class="w-1/3">One third width</div>

<!-- Height classes -->
<div class="h-screen">Full screen height</div>
<div class="h-64">Fixed height</div>
```

#### **Display and Layout**

```html
<!-- Flex layout (side by side) -->
<div class="flex items-center justify-between">
    <span>Left item</span>
    <span>Right item</span>
</div>

<!-- Grid layout (multiple columns) -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <!-- Items go here -->
</div>
```

#### **Responsive Design** (Mobile-first)

Your landing page uses responsive prefixes:

| Prefix | Means | Use when |
|--------|-------|----------|
| (no prefix) | Mobile | Default, applies to all screen sizes |
| `md:` | Medium screens (tablets) | 768px and above |
| `lg:` | Large screens (desktops) | 1024px and above |

**Example**:
```html
<!-- 4 columns on desktop, 2 on tablet, 1 on mobile -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
    <div>Item 4</div>
</div>
```

**This means**:
- Mobile (small phones): 1 column
- Tablet (medium): 2 columns
- Desktop (large): 4 columns

### Common Customizations

#### **Change Primary Color (Black to Blue)**

**Current button styling** (Lines 50-52):
```html
.btn-primary {
    @apply inline-flex items-center justify-center px-8 py-3 bg-black text-white font-semibold rounded-lg hover:bg-gray-800 transform hover:scale-105 transition-all duration-300 ease-out focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-black;
}
```

**To change to blue**:
```html
.btn-primary {
    @apply inline-flex items-center justify-center px-8 py-3 bg-blue-600 text-white font-semibold rounded-lg hover:bg-blue-700 transform hover:scale-105 transition-all duration-300 ease-out focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-600;
}
```

**What changed**:
- `bg-black` → `bg-blue-600` (button background)
- `hover:bg-gray-800` → `hover:bg-blue-700` (darker blue on hover)
- `focus:ring-black` → `focus:ring-blue-600` (focus outline color)

---

#### **Change Hero Section Height**

**Current** (Line 298):
```html
<section class="relative w-full h-screen md:h-[600px] overflow-hidden flex items-center justify-center">
```

**Explanation**:
- `h-screen` = Full screen height on mobile
- `md:h-[600px]` = 600px height on tablets and desktop

**To make it shorter**:
```html
<section class="relative w-full h-96 md:h-[500px] overflow-hidden flex items-center justify-center">
```

**Height options**:
- `h-screen` = Full screen
- `h-96` = 384px
- `h-80` = 320px
- `h-[600px]` = Custom 600px

---

#### **Change Feature Cards from 3 Columns to 2 Columns**

**Current** (Line 337):
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

**Change to 2 columns**:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
```

**Explanation**:
- `grid-cols-1` = 1 column on mobile
- `md:grid-cols-2` = 2 columns on tablet
- `lg:grid-cols-2` = 2 columns on desktop (changed from 3)

---

#### **Change Spacing/Padding**

**Current section padding** (Line 330):
```html
<section id="features" class="py-16 md:py-24 bg-white">
```

**To add more space**:
```html
<section id="features" class="py-24 md:py-32 bg-white">
```

**Spacing values**:
- `py-16` = 64px vertical padding
- `py-24` = 96px vertical padding
- `py-32` = 128px vertical padding

---

#### **Change Background Color of a Section**

**Current** (Line 560):
```html
<section id="faq" class="py-16 md:py-24 bg-gray-50">
```

**To change to light blue**:
```html
<section id="faq" class="py-16 md:py-24 bg-blue-50">
```

**Available background colors**:
- `bg-white` = White
- `bg-gray-50` = Very light gray
- `bg-gray-100` = Light gray
- `bg-blue-50` = Very light blue
- `bg-green-50` = Very light green

---

#### **Change Text Alignment**

**Current centered text** (Line 331):
```html
<div class="text-center mb-12 md:mb-16">
```

**To change to left-aligned**:
```html
<div class="text-left mb-12 md:mb-16">
```

**Alignment options**:
- `text-center` = Centered
- `text-left` = Left-aligned
- `text-right` = Right-aligned

---

#### **Change Button Size**

**Current button** (Line 313):
```html
<a href="https://ledx.com" class="btn-primary">Explore Collection</a>
```

**To make button larger**, modify the `.btn-primary` class (Lines 50-52):

**Current**:
```html
.btn-primary {
    @apply inline-flex items-center justify-center px-8 py-3 bg-black...
}
```

**Make larger**:
```html
.btn-primary {
    @apply inline-flex items-center justify-center px-12 py-4 bg-black...
}
```

**What changed**:
- `px-8` → `px-12` (horizontal padding - makes button wider)
- `py-3` → `py-4` (vertical padding - makes button taller)

---

#### **Change Feature Icon Size**

**Current** (Line 339):
```html
<div class="feature-icon">
    <i class="fas fa-lightbulb"></i>
</div>
```

**In the CSS** (Lines 80-82):
```html
.feature-icon {
    @apply text-4xl text-black mb-4;
}
```

**To make icons larger**:
```html
.feature-icon {
    @apply text-6xl text-black mb-4;
}
```

**Icon sizes**:
- `text-4xl` = Large
- `text-5xl` = Larger
- `text-6xl` = Very large

---

#### **Change Card Hover Effect**

**Current** (Lines 75-77):
```html
.card-hover {
    @apply transform hover:scale-105 hover:shadow-xl transition-all duration-300 ease-out;
}
```

**To make hover effect more dramatic**:
```html
.card-hover {
    @apply transform hover:scale-110 hover:shadow-2xl transition-all duration-300 ease-out;
}
```

**What changed**:
- `hover:scale-105` → `hover:scale-110` (grows more on hover)
- `hover:shadow-xl` → `hover:shadow-2xl` (bigger shadow)

---

### Responsive Design Tips

Your landing page is **mobile-first**. This means:

1. **Always write mobile styles first** (no prefix)
2. **Then add tablet styles** (with `md:`)
3. **Then add desktop styles** (with `lg:`)

**Example**:
```html
<!-- Mobile: 1 column, Tablet: 2 columns, Desktop: 3 columns -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
```

### Testing Your Changes

After modifying Tailwind classes:

1. **Save the file** (Ctrl+S or Cmd+S)
2. **Refresh your browser** (F5 or Cmd+R)
3. **Check on mobile** - Resize your browser window or use phone
4. **Check on tablet** - Set browser to 768px width
5. **Check on desktop** - Full browser width

---

## Fixing Broken Links

### Understanding Links in Your Page

Links are created with the `<a>` tag and the `href` attribute:

```html
<a href="https://ledx.com">Shop Now</a>
```

**Parts**:
- `<a>` = Link tag
- `href="..."` = Where the link goes
- Text between `<a>` and `</a>` = What displays

### Identifying All Links in Your Page

Here are **all the links** that need checking:

#### **1. Header Navigation Links** (Lines 256-260)

```html
<a href="#features" class="text-gray-700 hover:text-black transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-black transition-colors duration-300 font-medium">Benefits</a>
<a href="#faq" class="text-gray-700 hover:text-black transition-colors duration-300 font-medium">FAQ</a>
<a href="#contact" class="text-gray-700 hover:text-black transition-colors duration-300 font-medium">Contact</a>
```

**What these do**: These are **anchor links** - they scroll to sections on the same page. The `#` means "on this page."

**These are correct** - don't change them unless you rename sections.

---

#### **2. Search Button and CTA Links** (Lines 266-267)

```html
<a href="https://ledx.com" class="btn-primary">Shop Now</a>
```

**What this does**: Links to external website (ledx.com)

**To update**:
```html
<!-- Change from: -->
<a href="https://ledx.com" class="btn-primary">Shop Now</a>

<!-- Change to: -->
<a href="https://yourshop.com" class="btn-primary">Shop Now</a>
```

---

#### **3. Mobile Menu Links** (Lines 276-281)

```html
<a href="#features" class="block text-gray-700 hover:text-black transition-colors duration-300 font-medium py-2">Features</a>
<a href="#benefits" class="block text-gray-700 hover:text-black transition-colors duration-300 font-medium py-2">Benefits</a>
<a href="#faq" class="block text-gray-700 hover:text-black transition-colors duration-300 font-medium py-2">FAQ</a>
<a href="#contact" class="block text-gray-700 hover:text-black transition-colors duration-300 font-medium py-2">Contact</a>
<a href="https://ledx.com" class="btn-primary block text-center">Shop Now</a>
```

**Same as header** - anchor links for sections plus one external link to shop.

---

#### **4. Hero Section CTA Buttons** (Lines 313-314)

```html
<a href="https://ledx.com" class="btn-primary">Explore Collection</a>
<button class="btn-secondary" onclick="document.getElementById('features').scrollIntoView({ behavior: 'smooth' })">Learn More</button>
```

**First button**: External link to shop
**Second button**: Scrolls to Features section (no link needed)

---

#### **5. Features Section CTA Links** (Lines 351, 365, 379)

```html
<a href="https://ledx.com" class="btn-primary">Shop Free Delivery</a>
```

**Appears 3 times** - once in each feature card. All point to shop.

---

#### **6. Benefits Section CTA Links** (Lines 439, 470, 501)

```html
<a href="https://ledx.com" class="btn-primary">Shop Free Delivery</a>
<a href="https://ledx.com" class="btn-primary">Order Now</a>
<a href="https://ledx.com" class="btn-primary">Browse Quality Products</a>
```

**All point to shop** - update all three.

---

#### **7. CTA Section Buttons** (Lines 531-532)

```html
<a href="https://ledx.com" class="btn-primary">Start Shopping Today</a>
<button class="btn-secondary" onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' })">Get in Touch</button>
```

**First**: External link to shop
**Second**: Scrolls to Contact section

---

#### **8. Contact Section Links** (Lines 819-821)

```html
<a href="mailto:adminx@led.com" class="text-gray-700 hover:text-black transition-colors duration-300">adminx@led.com</a>

<a href="https://ledx.com" class="text-gray-700 hover:text-black transition-colors duration-300">https://ledx.com</a>
```

**First**: Email link - `mailto:` prefix sends email
**Second**: Website link

---

#### **9. Footer Links** (Lines 885-906)

**Quick Links**:
```html
<a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Features</a>
<a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Benefits</a>
<a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">FAQ</a>
<a href="https://ledx.com" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Shop</a>
```

**Customer Service**:
```html
<a href="#contact" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Contact Us</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Terms & Conditions</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Blog</a>
```

**Social Media** (Lines 910-925):
```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-white hover:text-gray-900 transition-all duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
<!-- More social links... -->
```

---

### Step-by-Step: Update All Shop Links

**Scenario**: You want to change all shop links from `ledx.com` to `myshop.com`

**Method 1: Find and Replace** (Easiest)

1. Open your `index.html` in a text editor
2. Press **Ctrl+H** (Windows) or **Cmd+Option+F** (Mac)
3. Find: `https://ledx.com`
4. Replace with: `https://myshop.com`
5. Click "Replace All"
6. Save the file

**Method 2: Manual Update**

Find each instance and update:

1. Line 267: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
2. Line 282: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
3. Line 313: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
4. Line 351: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
5. Line 365: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
6. Line 379: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
7. Line 439: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
8. Line 470: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
9. Line 501: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
10. Line 531: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
11. Line 821: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`
12. Line 895: `<a href="https://ledx.com"` → `<a href="https://myshop.com"`

---

### Step-by-Step: Update Email Address

**Scenario**: Change contact email from `adminx@led.com` to `support@yourcompany.com`

**Find and Replace Method**:

1. Press **Ctrl+H** (Windows) or **Cmd+Option+F** (Mac)
2. Find: `adminx@led.com`
3. Replace with: `support@yourcompany.com`
4. Click "Replace All"
5. Save

**Locations to check**:
- Line 820: In Contact section
- Line 955: In footer contact form handler

**Important**: When you replace the email in the footer, make sure both instances change:

```html
<!-- Line 820 - Display link -->
<a href="mailto:support@yourcompany.com" class="text-gray-700 hover:text-black transition-colors duration-300">support@yourcompany.com</a>

<!-- Line 955 - Form submission -->
window.location.href = mailtoLink; // This uses the email from the form
```

---

### Step-by-Step: Update Website Link

**Scenario**: Change website from `ledx.com` to `yourcompany.com`

**In Contact Section** (Line 821):
```html
<!-- Change from: -->
<a href="https://ledx.com" class="text-gray-700 hover:text-black transition-colors duration-300">https://ledx.com</a>

<!-- Change to: -->
<a href="https://yourcompany.com" class="text-gray-700 hover:text-black transition-colors duration-300">https://yourcompany.com</a>
```

**In Footer** (Line 895):
```html
<!-- Change from: -->
<a href="https://ledx.com" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Shop</a>

<!-- Change to: -->
<a href="https://yourcompany.com" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Shop</a>
```

---

### Step-by-Step: Update Social Media Links

**Scenario**: Add your actual social media profiles

**Facebook** (Line 910):
```html
<!-- Change from: -->
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-white hover:text-gray-900 transition-all duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- Change to: -->
<a href="https://facebook.com/yourpage" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-white hover:text-gray-900 transition-all duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

**Instagram** (Line 915):
```html
<!-- Change href="#" to: -->
href="https://instagram.com/yourprofile"
```

**Twitter** (Line 920):
```html
<!-- Change href="#" to: -->
href="https://twitter.com/yourhandle"
```

**YouTube** (Line 925):
```html
<!-- Change href="#" to: -->
href="https://youtube.com/yourchannel"
```

---

### Testing Links

After updating links:

1. **Save the file**
2. **Refresh browser** (F5)
3. **Click each link** to verify:
   - External links open in new tab
   - Email links open email client
   - Anchor links scroll to correct section
   - Social links go to your profiles

**Quick Link Test Checklist**:

- [ ] "Shop Now" buttons go to shop
- [ ] Navigation menu items scroll correctly
- [ ] "Contact Us" link scrolls to contact form
- [ ] Email link opens email client
- [ ] Website link goes to correct site
- [ ] Facebook link goes to your Facebook
- [ ] Instagram link goes to your Instagram
- [ ] Twitter link goes to your Twitter
- [ ] YouTube link goes to your YouTube
- [ ] Privacy Policy link works (see next section)
- [ ] Terms link works (see next section)

---

## Linking Privacy and Terms Pages

### Understanding What We're Creating

You need to create two new pages:
1. **privacy.html** - Your privacy policy
2. **terms.html** - Your terms of service

Then link them from your main `index.html` page.

### Step 1: Create the Privacy Policy Page

**Create a new file** named `privacy.html` in the same folder as `index.html`

**Copy this template** and save it as `privacy.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Photography SE Asia">
    <title>Privacy Policy - Photography SE Asia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <i class="fas fa-camera text-2xl text-black"></i>
                <a href="index.html" class="text-xl font-bold text-gray-900 hover:text-gray-700 transition-colors">Photography SE Asia</a>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-black transition-colors font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Introduction</h2>
                <p>Photography SE Asia ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Information We Collect</h2>
                <p>We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the Site or when you choose to participate in various activities related to the Site.</li>
                    <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase products from the Site.</li>
                    <li>Data From Social Networks: User information from social networks, including your name, your social network username, location, gender, birth date, email address, profile picture, and public data for contacts, if you connect your account to such social networks.</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Use of Your Information</h2>
                <p>Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Generate a personal profile about you so that future visits to the Site will be personalized as possible.</li>
                    <li>Increase the efficiency and operation of the Site.</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the Site.</li>
                    <li>Notify you of updates to the Site.</li>
                    <li>Offer new products, services, and/or recommendations to you.</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Disclosure of Your Information</h2>
                <p>We may share information we have collected about you in certain situations:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information about you is necessary to comply with the law, enforce our Site policies, or protect ours or others' rights, property, or safety.</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with third parties that perform services for us, including payment processing, data analysis, email delivery, hosting services, customer service, and marketing assistance.</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Security of Your Information</h2>
                <p>We use administrative, technical, and physical security measures to help protect your personal information. While we have taken reasonable steps to secure the personal information you provide to us, please be aware that despite our efforts, no security measures are perfect or impenetrable.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Contact Us</h2>
                <p>If you have questions or comments about this Privacy Policy, please contact us at:</p>
                <p class="mt-4">
                    <strong>Photography SE Asia</strong><br>
                    Email: <a href="mailto:adminx@led.com" class="text-blue-600 hover:underline">adminx@led.com</a><br>
                    Website: <a href="https://ledx.com" class="text-blue-600 hover:underline">https://ledx.com</a>
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-100 py-8 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 text-sm">&copy; 2024 Photography SE Asia. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

**Create a new file** named `terms.html` in the same folder as `index.html`

**Copy this template** and save it as `terms.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Photography SE Asia">
    <title>Terms of Service - Photography SE Asia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <i class="fas fa-camera text-2xl text-black"></i>
                <a href="index.html" class="text-xl font-bold text-gray-900 hover:text-gray-700 transition-colors">Photography SE Asia</a>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-black transition-colors font-medium">Back to Home</a>
        </nav>
    </header>

    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>Permission is granted to temporarily download one copy of the materials (information or software) on Photography SE Asia's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>The materials on Photography SE Asia's website are provided on an 'as is' basis. Photography SE Asia makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>In no event shall Photography SE Asia or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the website, even if Photography SE Asia or an authorized representative has been notified orally or in writing of the possibility of such damage.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>The materials appearing on Photography SE Asia's website could include technical, typographical, or photographic errors. Photography SE Asia does not warrant that any of the materials on the website are accurate, complete, or current. Photography SE Asia may make changes to the materials contained on its website at any time without notice.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>Photography SE Asia has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Photography SE Asia of the site. Use of any such linked website is at the user's own risk.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>Photography SE Asia may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>These terms and conditions are governed by and construed in accordance with the laws of Singapore, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">Contact Us</h2>
                <p>If you have any questions about these Terms of Service, please contact us at:</p>
                <p class="mt-4">
                    <strong>Photography SE Asia</strong><br>
                    Email: <a href="mailto:adminx@led.com" class="text-blue-600 hover:underline">adminx@led.com</a><br>
                    Website: <a href="https://ledx.com" class="text-blue-600 hover:underline">https://ledx.com</a>
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-100 py-8 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 text-sm">&copy; 2024 Photography SE Asia. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Update Footer Links in index.html

Now you need to update your main `index.html` to link to these new pages.

**Find the Footer** (Lines 903-906):

```html
<!-- Current - Links don't work -->
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Terms & Conditions</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Blog</a></li>
```

**Replace with**:

```html
<!-- Updated - Links now work -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Terms & Conditions</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Blog</a></li>
```

**What changed**:
- `href="#"` → `href="privacy.html"` (Privacy Policy)
- `href="#"` → `href="terms.html"` (Terms & Conditions)
- Blog link stays as `#` since you don't have a blog page yet

---

### Step 4: Update Footer Bottom Links in index.html

**Find the Footer Bottom** (Lines 933-938):

```html
<!-- Current - These links don't work -->
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Terms of Service</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Cookie Settings</a>
```

**Replace with**:

```html
<!-- Updated - Privacy and Terms links now work -->
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Terms of Service</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-sm">Cookie Settings</a>
```

---

### Complete File Structure After Setup

After completing these steps, your folder should look like:

```
your-project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy page)
├── terms.html (terms of service page)
└── README.md (this documentation)
```

---

### Testing Your Policy Pages

**Test the links**:

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click "Privacy Policy" - should open `privacy.html`
4. Click "Back to Home" - should return to `index.html`
5. Click "Terms & Conditions" - should open `terms.html`
6. Click "Back to Home" - should return to `index.html`

**Verify all links work**:
- [ ] Privacy Policy link in footer customer service section
- [ ] Terms & Conditions link in footer customer service section
- [ ] Privacy Policy link in footer bottom
- [ ] Terms of Service link in footer bottom
- [ ] Back to Home link on privacy.html
- [ ] Back to Home link on terms.html

---

### Customizing Privacy and Terms Content

The templates provided are generic. You should customize them with your actual policies:

**For Privacy Policy**, update:
- The types of data you collect
- How you use the data
- Your data retention policies
- How users can request their data
- Your contact information

**For Terms of Service**, update:
- Your return policy details
- Shipping policy specifics
- Warranty information
- Your company's specific terms
- Governing law (if different from Singapore)

**Example - Customizing Contact Info**:

In both `privacy.html` and `terms.html`, find:

```html
<strong>Photography SE Asia</strong><br>
Email: <a href="mailto:adminx@led.com" class="text-blue-600 hover:underline">adminx@led.com</a><br>
Website: <a href="https://ledx.com" class="text-blue-600 hover:underline">https://ledx.com</a>
```

Replace with your actual contact information:

```html
<strong>Your Company Name</strong><br>
Email: <a href="mailto:your@email.com" class="text-blue-600 hover:underline">your@email.com</a><br>
Website: <a href="https://yourwebsite.com" class="text-blue-600 hover:underline">https://yourwebsite.com</a>
```

---

## Common Customizations

### Changing the Announcement Bar Message

**Location**: Line 246

```html
<!-- Current -->
<p>🚚 Free worldwide shipping on orders over $50. Fast delivery in 5 days!</p>

<!-- Change to seasonal message -->
<p>🎉 Holiday Sale: 30% off all equipment. Limited time only!</p>

<!-- Or change to standard message -->
<p>📦 Free shipping on all orders. Fast delivery guaranteed!</p>
```

---

### Adding New Feature Cards

**To add a 4th feature card**, find the Features section (Line 337) and add a new card:

```html
<!-- Add after the third card (after line 379) -->

<div class="card-hover bg-white p-8 rounded-xl border border-gray-200 hover:border-gray-300 transition-colors duration-300">
    <div class="feature-icon">
        <i class="fas fa-headset"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3">24/7 Support</h3>
    <p class="text-gray-600 leading-relaxed mb-4">Round-the-clock customer support to help you with any questions or issues.</p>
    <ul class="space-y-2 text-sm text-gray-700">
        <li class="flex items-center"><i class="fas fa-check text-black mr-2"></i>Live chat support</li>
        <li class="flex items-center"><i class="fas fa-check text-black mr-2"></i>Email assistance</li>
        <li class="flex items-center"><i class="fas fa-check text-black mr-2"></i>Phone support</li>
    </ul>
</div>
```

**Then update the grid** (Line 337) to 4 columns on large screens:

```html
<!-- Change from: -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

<!-- Change to: -->
<div