# 3D Scan Pro Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the 3D Scan Pro landing page. Whether you're updating text, fixing links, or adding new pages, you'll find step-by-step instructions tailored to this specific website.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Part 1: Updating Text and Tailwind CSS Classes](#part-1-updating-text-and-tailwind-css-classes)
3. [Part 2: Fixing Broken Links](#part-2-fixing-broken-links)
4. [Part 3: Linking Privacy and Terms Pages](#part-3-linking-privacy-and-terms-pages)
5. [Troubleshooting Guide](#troubleshooting-guide)
6. [Best Practices](#best-practices)

---

## Quick Start Overview

### What You're Working With

The 3D Scan Pro landing page is built using:
- **HTML**: The structure and content of the page
- **Tailwind CSS**: A utility-first CSS framework that controls styling and layout
- **Font Awesome Icons**: For visual icons throughout the page
- **Vanilla JavaScript**: For interactive features like the mobile menu

### File Structure You'll Need

```
your-project-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy Policy - you'll create this)
├── terms.html          (Terms of Service - you'll create this)
└── blog.html           (Blog page - referenced but not included)
```

### Key Concept: Tailwind CSS Classes

Throughout this page, styling is controlled by classes like `bg-blue-600`, `text-white`, and `p-8`. These are **Tailwind utility classes** that control:
- **Colors**: `bg-blue-600` (background color)
- **Text**: `text-white` (text color), `text-xl` (text size)
- **Spacing**: `p-8` (padding), `m-6` (margin)
- **Responsive Design**: `sm:text-5xl` (changes on small screens)

You'll rarely need to change these unless you want to redesign the page.

---

## Part 1: Updating Text and Tailwind CSS Classes

### 1.1 Understanding the Page Structure

The landing page is divided into clear sections. Here's where to find and update each one:

| Section | Location in HTML | Purpose |
|---------|-----------------|---------|
| **Header/Navigation** | Lines 62-102 | Site logo, menu links, mobile menu |
| **Hero Section** | Lines 104-152 | Main headline, subheading, CTA buttons |
| **Features Section** | Lines 154-228 | Three feature cards with icons |
| **Benefits Section** | Lines 230-326 | Four benefit cards with statistics |
| **CTA Section** | Lines 328-343 | Call-to-action with background image |
| **Testimonials** | Lines 345-424 | Four customer testimonials |
| **About Us** | Lines 426-481 | Company information and stats |
| **Final CTA** | Lines 483-502 | Last call-to-action section |
| **Footer** | Lines 504-593 | Links, social media, legal info |

---

### 1.2 Updating the Company Name and Logo

**Current Location**: Lines 68-72 (Header) and Lines 551-556 (Footer)

The company name "3D Scan Pro" appears in two places. Here's how to change it:

#### Step 1: Update the Header Logo/Name

**Find this code** (around line 68-72):
```html
<div class="flex items-center space-x-2">
    <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-800 rounded-lg flex items-center justify-center">
        <i class="fas fa-cube text-white text-lg"></i>
    </div>
    <span class="text-xl font-bold text-gray-900">3D Scan Pro</span>
</div>
```

**To change it**, replace `3D Scan Pro` with your company name:
```html
<span class="text-xl font-bold text-gray-900">Your Company Name</span>
```

**Example**: If your company is "CloudScan Solutions", change it to:
```html
<span class="text-xl font-bold text-gray-900">CloudScan Solutions</span>
```

#### Step 2: Update the Footer Logo/Name

**Find this code** (around line 551-556):
```html
<div class="flex items-center space-x-2 mb-6">
    <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-blue-700 rounded-lg flex items-center justify-center">
        <i class="fas fa-cube text-white text-lg"></i>
    </div>
    <span class="text-xl font-bold text-white">3D Scan Pro</span>
</div>
```

**Change it the same way**:
```html
<span class="text-xl font-bold text-white">Your Company Name</span>
```

**Why two places?** The header stays visible at the top of the page, and the footer appears at the bottom. Users should see your consistent branding in both locations.

---

### 1.3 Updating the Main Headline (Hero Section)

**Current Location**: Lines 113-117

This is the biggest, most important text on your page.

**Find this code**:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    3D Scanning On-Site: <span class="gradient-text">Capture Reality Now!</span>
</h1>
```

**What each part does**:
- `text-4xl sm:text-5xl lg:text-6xl`: Makes text larger on bigger screens
- `font-bold`: Makes text bold
- `text-gray-900`: Dark gray color
- `mb-6`: Adds margin (space) below the headline
- `gradient-text`: Special class that creates a blue gradient effect on the text

**To update it**, change the text between the `<h1>` tags:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Your New Headline: <span class="gradient-text">Your Tagline Here!</span>
</h1>
```

**Example**:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Professional Surveying Made Easy: <span class="gradient-text">Accuracy in Minutes!</span>
</h1>
```

**Pro Tip**: Keep the `<span class="gradient-text">` tags around your tagline to maintain the blue gradient effect on that portion.

---

### 1.4 Updating the Hero Subheading

**Current Location**: Lines 119-123

This is the descriptive paragraph under the main headline.

**Find this code**:
```html
<p class="text-lg sm:text-xl text-gray-600 leading-relaxed mb-8 max-w-3xl mx-auto">
    Bring the power of precision 3D scanning directly to your project site. Our advanced on-site scanning solutions deliver accurate data, faster workflows, and dramatically reduced rework – all guaranteed to transform your project outcomes.
</p>
```

**What each part does**:
- `text-lg sm:text-xl`: Text size (larger on small screens)
- `text-gray-600`: Medium gray color
- `leading-relaxed`: Adds space between lines for readability
- `mb-8`: Margin below
- `max-w-3xl mx-auto`: Limits width and centers it

**To update it**, replace the paragraph text:
```html
<p class="text-lg sm:text-xl text-gray-600 leading-relaxed mb-8 max-w-3xl mx-auto">
    Your new description goes here. Explain your service, highlight key benefits, and tell visitors why they should care.
</p>
```

**Example**:
```html
<p class="text-lg sm:text-xl text-gray-600 leading-relaxed mb-8 max-w-3xl mx-auto">
    Transform your surveying process with cloud-based technology. Get accurate measurements, instant reports, and seamless team collaboration—all from your mobile device.
</p>
```

---

### 1.5 Updating Feature Cards

**Current Location**: Lines 167-228 (Three feature cards)

Each feature card has an icon, title, description, and bullet points.

#### Updating Feature 1: Portable Scanners

**Find this code** (lines 167-189):
```html
<div class="feature-card">
    <div class="w-16 h-16 bg-gradient-to-br from-blue-100 to-blue-50 rounded-xl flex items-center justify-center mb-6">
        <i class="fas fa-mobile-alt text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Portable Scanners</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Lightweight, ergonomic scanning equipment that's easy to transport and deploy across any job site. Our portable scanners weigh less than 5 kg yet deliver enterprise-grade precision and accuracy.
    </p>
    <ul class="space-y-2 text-sm text-gray-600">
        <li class="flex items-start">
            <i class="fas fa-check text-green-500 mr-3 mt-1"></i>
            <span>Ultra-compact design for maximum mobility</span>
        </li>
        <li class="flex items-start">
            <i class="fas fa-check text-green-500 mr-3 mt-1"></i>
            <span>Extended battery life up to 8 hours</span>
        </li>
        <li class="flex items-start">
            <i class="fas fa-check text-green-500 mr-3 mt-1"></i>
            <span>One-person operation capability</span>
        </li>
    </ul>
</div>
```

**To update this feature card**:

1. **Change the icon** (line 173):
   - Find: `<i class="fas fa-mobile-alt text-blue-600 text-2xl"></i>`
   - Replace with a different Font Awesome icon
   - Visit [fontawesome.com/icons](https://fontawesome.com/icons) to find icons
   - Example: `<i class="fas fa-microchip text-blue-600 text-2xl"></i>` (microchip icon)

2. **Change the title** (line 176):
   - Find: `<h3 class="text-xl font-bold text-gray-900 mb-4">Portable Scanners</h3>`
   - Replace: `<h3 class="text-xl font-bold text-gray-900 mb-4">Your Feature Title</h3>`

3. **Change the description** (lines 177-180):
   - Replace the paragraph text with your description

4. **Update the bullet points** (lines 181-191):
   - Each bullet is an `<li>` tag
   - Replace the `<span>` text with your bullet point
   - To add more bullets, copy an entire `<li>` block and paste it, then edit the text
   - To remove bullets, delete the entire `<li>` block

**Complete Example** - Changing Feature 1 to "Cloud Integration":
```html
<div class="feature-card">
    <div class="w-16 h-16 bg-gradient-to-br from-blue-100 to-blue-50 rounded-xl flex items-center justify-center mb-6">
        <i class="fas fa-cloud text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Cloud Integration</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Seamlessly sync your data to the cloud for instant access from anywhere. Your team can collaborate in real-time without worrying about file transfers or version control.
    </p>
    <ul class="space-y-2 text-sm text-gray-600">
        <li class="flex items-start">
            <i class="fas fa-check text-green-500 mr-3 mt-1"></i>
            <span>Automatic backup and version history</span>
        </li>
        <li class="flex items-start">
            <i class="fas fa-check text-green-500 mr-3 mt-1"></i>
            <span>Access from any device, anywhere</span>
        </li>
        <li class="flex items-start">
            <i class="fas fa-check text-green-500 mr-3 mt-1"></i>
            <span>Enterprise-grade security</span>
        </li>
    </ul>
</div>
```

#### Updating Features 2 and 3

Follow the same process for the other two feature cards (lines 192-214 for Feature 2, lines 216-228 for Feature 3).

---

### 1.6 Updating Benefit Cards

**Current Location**: Lines 249-326

The benefits section has four cards with icons, titles, descriptions, and highlighted statistics.

**Find a benefit card** (example: lines 249-267):
```html
<div class="flex gap-6">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-14 w-14 rounded-lg bg-blue-600 shadow-lg">
            <i class="fas fa-tachometer-alt text-white text-xl"></i>
        </div>
    </div>
    <div>
        <h3 class="text-2xl font-bold text-gray-900 mb-3">Accelerated Project Timelines</h3>
        <p class="text-gray-600 leading-relaxed mb-4">
            Reduce project duration by up to 40% through faster data acquisition and elimination of manual measurement errors. Real-time scanning means you capture accurate information in a single pass, eliminating the need for time-consuming re-scans and corrections.
        </p>
        <div class="bg-white rounded-lg p-4 border-l-4 border-blue-600">
            <p class="text-sm text-gray-700"><strong>Average time savings:</strong> 2-3 weeks per project phase</p>
        </div>
    </div>
</div>
```

**To update each benefit**:

1. **Change the icon** (line 255):
   - Find: `<i class="fas fa-tachometer-alt text-white text-xl"></i>`
   - Replace with your chosen icon from [fontawesome.com/icons](https://fontawesome.com/icons)

2. **Change the icon background color** (line 254):
   - Find: `bg-blue-600` (currently blue)
   - Replace with: `bg-green-600` (green), `bg-purple-600` (purple), `bg-orange-600` (orange), etc.
   - **Note**: Look at the other benefits - they use different colors to provide visual variety

3. **Change the title** (line 259):
   - Find: `<h3 class="text-2xl font-bold text-gray-900 mb-3">Accelerated Project Timelines</h3>`
   - Replace the title text

4. **Change the description** (lines 260-263):
   - Replace the paragraph text

5. **Update the highlight box** (lines 264-266):
   - Find: `<p class="text-sm text-gray-700"><strong>Average time savings:</strong> 2-3 weeks per project phase</p>`
   - Replace the bold label and the statistic

**Example** - Updating Benefit 1 to focus on cost savings:
```html
<div class="flex gap-6">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-14 w-14 rounded-lg bg-green-600 shadow-lg">
            <i class="fas fa-coins text-white text-xl"></i>
        </div>
    </div>
    <div>
        <h3 class="text-2xl font-bold text-gray-900 mb-3">Immediate Cost Reduction</h3>
        <p class="text-gray-600 leading-relaxed mb-4">
            Eliminate expensive measurement errors and rework. Our precision technology ensures you get it right the first time, saving money on materials, labor, and project delays.
        </p>
        <div class="bg-white rounded-lg p-4 border-l-4 border-green-600">
            <p class="text-sm text-gray-700"><strong>Average savings:</strong> $50,000+ per project</p>
        </div>
    </div>
</div>
```

---

### 1.7 Updating Testimonials

**Current Location**: Lines 365-424

Each testimonial has a 5-star rating, quote, and author information.

**Find a testimonial** (example: lines 368-387):
```html
<div class="testimonial-card">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "The 3D scanning solution has been a game-changer for our construction projects. We've cut our survey time in half and eliminated costly measurement errors. The real-time data processing means we can make decisions on-site instead of waiting days for reports. Highly recommended!"
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-gray-900">Michael Chen</p>
        <p class="text-sm text-gray-600">Project Manager, BuildRight Construction</p>
    </div>
</div>
```

**To update a testimonial**:

1. **Change the star rating** (lines 370-377):
   - For 4 stars, remove one `<i class="fas fa-star"></i>` line
   - For 3 stars, remove two star lines
   - Don't go below 3 stars for social proof!

2. **Change the quote** (lines 378-382):
   - Replace the text between the `<p>` tags
   - Keep the opening and closing quotation marks for clarity

3. **Update the author name** (line 385):
   - Find: `<p class="font-semibold text-gray-900">Michael Chen</p>`
   - Replace: `<p class="font-semibold text-gray-900">Your Client Name</p>`

4. **Update the author title/company** (line 386):
   - Find: `<p class="text-sm text-gray-600">Project Manager, BuildRight Construction</p>`
   - Replace: `<p class="text-sm text-gray-600">Their Title, Their Company</p>`

**Example** - New testimonial:
```html
<div class="testimonial-card">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "Outstanding service! The team was professional, the equipment worked flawlessly, and we saved two weeks on our renovation project. The accuracy was exactly what we needed for our specifications."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-gray-900">Jessica Martinez</p>
        <p class="text-sm text-gray-600">Director of Operations, Heritage Renovations LLC</p>
    </div>
</div>
```

---

### 1.8 Updating the About Section

**Current Location**: Lines 436-481

This section includes company description, mission statement, and key statistics.

**Find the main text** (lines 448-463):
```html
<p class="text-lg text-gray-700 leading-relaxed">
    Founded in 2015 by a team of surveying professionals and software engineers, 3D Scan Pro emerged from a simple observation: the construction and surveying industries were still relying on outdated measurement techniques that were slow, error-prone, and expensive. Our founders recognized that the convergence of advanced scanning hardware, cloud computing, and real-time processing created an unprecedented opportunity to transform how projects are documented and managed. What started as a small startup with a single office has grown into a trusted partner for hundreds of organizations worldwide, serving everyone from individual contractors to Fortune 500 companies. Our journey has been driven by an unwavering commitment to innovation and customer success.
</p>

<p class="text-lg text-gray-700 leading-relaxed">
    Today, 3D Scan Pro stands as the industry leader in on-site 3D scanning solutions, guided by core values of precision, reliability, and customer empowerment. We believe that accurate data is the foundation of successful projects, and we're committed to making professional-grade scanning technology accessible to organizations of all sizes. Our mission is to eliminate inefficiency, reduce costly errors, and enable teams to work smarter through the power of precise 3D data. Every product we develop, every service we deliver, and every partnership we build reflects our dedication to transforming the way the world captures, analyzes, and acts on spatial information. We don't just provide equipment – we provide the tools and support necessary for our clients to achieve their most ambitious project goals.
</p>
```

**To update**: Simply replace the paragraph text with your company's story.

**Update the statistics** (lines 465-481):
```html
<div class="mt-12 pt-12 border-t border-gray-300 grid grid-cols-1 md:grid-cols-3 gap-8">
    <div class="text-center">
        <div class="text-4xl font-bold text-blue-600 mb-2">500+</div>
        <p class="text-gray-600">Active Clients Worldwide</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-bold text-blue-600 mb-2">2M+</div>
        <p class="text-gray-600">Projects Completed</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-bold text-blue-600 mb-2">99.8%</div>
        <p class="text-gray-600">Customer Satisfaction Rate</p>
    </div>
</div>
```

**To update statistics**:
- Replace `500+` with your actual number
- Replace `Active Clients Worldwide` with your stat label
- Update all three statistics boxes

**Example**:
```html
<div class="mt-12 pt-12 border-t border-gray-300 grid grid-cols-1 md:grid-cols-3 gap-8">
    <div class="text-center">
        <div class="text-4xl font-bold text-blue-600 mb-2">1,200+</div>
        <p class="text-gray-600">Successful Projects</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-bold text-blue-600 mb-2">25+</div>
        <p class="text-gray-600">Years Combined Experience</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-bold text-blue-600 mb-2">98%</div>
        <p class="text-gray-600">Client Retention Rate</p>
    </div>
</div>
```

---

### 1.9 Understanding Tailwind CSS Classes for Design Customization

If you want to change colors, spacing, or other design elements, here are the most common Tailwind classes used on this page:

#### Color Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `bg-blue-600` | Blue background | `<div class="bg-blue-600">` |
| `text-white` | White text | `<p class="text-white">` |
| `text-gray-900` | Dark gray text | `<h1 class="text-gray-900">` |
| `border-gray-200` | Light gray border | `<div class="border-gray-200">` |
| `hover:bg-blue-700` | Darker blue on hover | Button that changes on hover |

**To change colors**, replace the color name:
- Blues: `blue-50`, `blue-100`, `blue-600`, `blue-700`, `blue-800`
- Greens: `green-500`, `green-600`
- Purples: `purple-600`
- Oranges: `orange-600`
- Grays: `gray-50`, `gray-100`, `gray-600`, `gray-900`

#### Spacing Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `p-8` | Padding (space inside) | `<div class="p-8">` |
| `m-6` | Margin (space outside) | `<div class="m-6">` |
| `mb-4` | Margin below | `<h3 class="mb-4">` |
| `mt-12` | Margin top | `<div class="mt-12">` |
| `gap-8` | Space between items | `<div class="gap-8">` |

#### Text Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-xl` | Large text | `<p class="text-xl">` |
| `text-4xl` | Extra large text | `<h1 class="text-4xl">` |
| `font-bold` | Bold text | `<p class="font-bold">` |
| `font-semibold` | Semi-bold text | `<p class="font-semibold">` |

#### Responsive Classes

These classes make your page work on different screen sizes:

| Class | What It Does |
|-------|-------------|
| `sm:text-5xl` | Large text on small screens and up |
| `md:grid-cols-2` | 2 columns on medium screens and up |
| `lg:text-6xl` | Extra large text on large screens |
| `hidden md:flex` | Hidden by default, visible on medium screens |

**Example**: `<h1 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl">`
- On mobile: text-3xl (smaller)
- On small screens: text-4xl
- On medium screens: text-5xl
- On large screens: text-6xl (largest)

---

## Part 2: Fixing Broken Links

### 2.1 Understanding Links on This Page

A link is created with the `<a>` tag and the `href` attribute. Here's what a link looks like:

```html
<a href="https://example.com">Click Here</a>
```

- `<a>` = starts a link
- `href="..."` = where the link goes
- `</a>` = ends the link
- The text between `<a>` and `</a>` is what visitors see and click

### 2.2 Identifying All Links on the Page

Here's a complete list of all links on the 3D Scan Pro landing page and their current status:

#### Navigation Menu Links (Lines 80-87)

| Link Text | Current href | Status | Line |
|-----------|-------------|--------|------|
| Features | `#features` | ✓ Works (internal anchor) | 80 |
| Benefits | `#benefits` | ✓ Works (internal anchor) | 81 |
| Testimonials | `#testimonials` | ✓ Works (internal anchor) | 82 |
| About | `#about` | ✓ Works (internal anchor) | 83 |
| Get Started | `mailto:iainhmunro@gmail.com` | ⚠️ Needs update | 84 |

#### Hero Section Buttons (Lines 126-134)

| Link Text | Current href | Status | Line |
|-----------|-------------|--------|------|
| Start Your Project Today | `https://example.com` | ❌ Broken (placeholder) | 126 |
| Learn More | `#features` | ✓ Works (internal anchor) | 130 |

#### CTA Section Button (Line 340)

| Link Text | Current href | Status | Line |
|-----------|-------------|--------|------|
| Request a Demo Today | `https://example.com` | ❌ Broken (placeholder) | 340 |

#### Final CTA Section Buttons (Lines 494-502)

| Link Text | Current href | Status | Line |
|-----------|-------------|--------|------|
| Schedule a Demo | `https://example.com` | ❌ Broken (placeholder) | 494 |
| Contact Us | `mailto:iainhmunro@gmail.com` | ⚠️ Needs update | 498 |

#### Footer Links (Lines 539-593)

| Link Text | Current href | Status | Line |
|-----------|-------------|--------|------|
| Privacy Policy | `privacy.html` | ⚠️ File doesn't exist yet | 540 |
| Terms of Service | `terms.html` | ⚠️ File doesn't exist yet | 541 |
| Blog | `blog.html` | ❌ File doesn't exist | 542 |
| Pricing | `https://example.com` | ❌ Broken (placeholder) | 545 |
| Case Studies | `https://example.com` | ❌ Broken (placeholder) | 546 |
| Careers | `https://example.com` | ❌ Broken (placeholder) | 549 |
| Contact | `https://example.com` | ❌ Broken (placeholder) | 550 |
| Support | `https://example.com` | ❌ Broken (placeholder) | 551 |
| Cookie Policy | `https://example.com` | ❌ Broken (placeholder) | 574 |
| Data Processing | `https://example.com` | ❌ Broken (placeholder) | 575 |
| Compliance | `https://example.com` | ❌ Broken (placeholder) | 576 |

---

### 2.3 How to Fix Each Type of Link

#### Type 1: Fixing "example.com" Placeholder Links

These are external links that point to pages outside your website. They currently say `https://example.com`, which doesn't work.

**Step 1: Identify the link you want to fix**

Example - "Start Your Project Today" button (Line 126):
```html
<a href="https://example.com" class="btn-primary">
    <i class="fas fa-arrow-right mr-2"></i>Start Your Project Today
</a>
```

**Step 2: Replace the href with your actual URL**

If you want this button to go to your sales page at `https://yourdomain.com/contact`, change it to:
```html
<a href="https://yourdomain.com/contact" class="btn-primary">
    <i class="fas fa-arrow-right mr-2"></i>Start Your Project Today
</a>
```

**Common External Links to Update**:

1. **"Start Your Project Today"** (Line 126):
   ```html
   <!-- Change from: -->
   <a href="https://example.com" class="btn-primary">
   
   <!-- To: -->
   <a href="https://yourdomain.com/get-started" class="btn-primary">
   ```

2. **"Request a Demo Today"** (Line 340):
   ```html
   <!-- Change from: -->
   <a href="https://example.com" class="inline-block px-8 py-4...">
   
   <!-- To: -->
   <a href="https://yourdomain.com/demo" class="inline-block px-8 py-4...">
   ```

3. **"Schedule a Demo"** (Line 494):
   ```html
   <!-- Change from: -->
   <a href="https://example.com" class="px-8 py-4 bg-white...">
   
   <!-- To: -->
   <a href="https://yourdomain.com/schedule" class="px-8 py-4 bg-white...">
   ```

#### Type 2: Fixing Email Links

These are `mailto:` links that open the user's email client. Currently, they go to `iainhmunro@gmail.com`.

**Step 1: Find the email link**

Example - "Get Started" in header (Line 84):
```html
<a href="mailto:iainhmunro@gmail.com" class="btn-primary">Get Started</a>
```

**Step 2: Replace with your email address**

```html
<a href="mailto:your-email@yourdomain.com" class="btn-primary">Get Started</a>
```

**Step 3: Find all email links and update them**

There are two email links on this page:
1. Line 84: Header "Get Started" button
2. Line 498: Footer "Contact Us" button

**Complete Example** - Updating all email links:

**Before**:
```html
<!-- Line 84 -->
<a href="mailto:iainhmunro@gmail.com" class="btn-primary">Get Started</a>

<!-- Line 498 -->
<a href="mailto:iainhmunro@gmail.com" class="px-8 py-4 bg-blue-500...">
    <i class="fas fa-envelope mr-2"></i>Contact Us
</a>
```

**After**:
```html
<!-- Line 84 -->
<a href="mailto:sales@yourdomain.com" class="btn-primary">Get Started</a>

<!-- Line 498 -->
<a href="mailto:sales@yourdomain.com" class="px-8 py-4 bg-blue-500...">
    <i class="fas fa-envelope mr-2"></i>Contact Us
</a>
```

---

### 2.4 Step-by-Step: Complete Link Fix Checklist

Here's a complete checklist for fixing all broken links on this page:

#### Step 1: Update All External Links (5 minutes)

- [ ] Line 126: "Start Your Project Today" → Change to your sales/contact page
- [ ] Line 340: "Request a Demo Today" → Change to your demo booking page
- [ ] Line 494: "Schedule a Demo" → Change to your calendar/booking system

**How to do it**:
1. Open your `index.html` file in a text editor
2. Use Ctrl+F (or Cmd+F on Mac) to search for `https://example.com`
3. For each result, replace it with your actual URL
4. Save the file

#### Step 2: Update All Email Links (2 minutes)

- [ ] Line 84: "Get Started" button → Change to your email
- [ ] Line 498: "Contact Us" button → Change to your email

**How to do it**:
1. Use Ctrl+F to search for `mailto:iainhmunro@gmail.com`
2. Replace each instance with `mailto:your-email@yourdomain.com`
3. Save the file

#### Step 3: Create Placeholder Pages (Optional but Recommended)

Some links point to pages that don't exist yet:
- [ ] `privacy.html` (Privacy Policy)
- [ ] `terms.html` (Terms of Service)
- [ ] `blog.html` (Blog)

We'll handle these in Part 3.

---

### 2.5 Testing Your Links

After updating links, test them to make sure they work:

**For external links**:
1. Open your page in a web browser
2. Click each button
3. Verify it goes to the correct page
4. If it doesn't work, check that you used the full URL (including `https://`)

**For email links**:
1. Click the email link
2. Your default email client should open
3. The "To:" field should be pre-filled with your email address

**For internal links** (like `#features`):
1. Click the link
2. The page should scroll to that section
3. The URL should change to include `#features`

---

## Part 3: Linking Privacy and Terms Pages

### 3.1 Why You Need Privacy and Terms Pages

Privacy Policy and Terms of Service pages are:
- **Legally important**: They protect your business and set expectations with users
- **Trust-building**: They show you're a legitimate, professional business
- **SEO-friendly**: Search engines favor sites with proper legal pages
- **Already linked**: Your footer already references them, they just need to be created

### 3.2 Current Links to Privacy and Terms Pages

**In the Footer** (Lines 539-541 and 573-576):

```html
<!-- Product Links Section -->
<li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Pricing</a></li>

<!-- Legal Links Section -->
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
<li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Cookie Policy</a></li>

<!-- Bottom Footer -->
<a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy</a>
<a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms</a>
```

**Good news**: The links are already set up correctly! They point to `privacy.html` and `terms.html`. You just need to create these files.

---

### 3.3 Creating the Privacy Policy Page

#### Step 1: Create a New File

1. Open your text editor (same one you use for `index.html`)
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`

#### Step 2: Add the Basic Structure

Copy this template into your `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for 3D Scan Pro">
    <title>Privacy Policy | 3D Scan Pro</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-800 rounded-lg flex items-center justify-center">
                    <i class="fas fa-cube text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-gray-900">3D Scan Pro</span>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 font-medium transition-colors duration-300 hover:text-blue-600">Home</a>
                <a href="index.html#features" class="text-gray-700 font-medium transition-colors duration-300 hover:text-blue-600">Features</a>
                <a href="index.html#about" class="text-gray-700 font-medium transition-colors duration-300 hover:text-blue-600">About</a>
                <a href="mailto:sales@yourdomain.com" class="px-8 py-4 bg-blue-600 text-white font-semibold rounded-lg transition-all duration-300 hover:bg-blue-700 cursor-pointer">Contact</a>
            </div>
            
            <button class="mobile-menu-button md:hidden p-2 rounded-lg hover:bg-gray-100 transition-colors duration-300">
                <i class="fas fa-bars text-gray-900 text-xl"></i>
            </button>
            
            <div class="mobile-menu hidden absolute top-full left-0 right-0 bg-white shadow-lg md:hidden">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col space-y-4">
                    <a href="index.html" class="text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-blue-600">Home</a>
                    <a href="index.html#features" class="text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-blue-600">Features</a>
                    <a href="index.html#about" class="text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-blue-600">About</a>
                    <a href="mailto:sales@yourdomain.com" class="px-8 py-4 bg-blue-600 text-white font-semibold rounded-lg transition-all duration-300 hover:bg-blue-700 cursor-pointer text-center">Contact</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 sm:py-24">
        <h1 class="text-4xl sm:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg max-w-none text-gray-700 space-y-8">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>
                    3D Scan Pro ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, and other contact information you voluntarily provide</li>
                    <li><strong>Device Information:</strong> Information about your device, including IP address, browser type, and operating system</li>
                    <li><strong>Usage Data:</strong> Information about how you interact with our website, including pages visited and time spent</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. How We Use Your Information</h2>
                <p>
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Create and manage your account</li>
                    <li>Process your transactions and send related information</li>
                    <li>Email you regarding updates or informational communications</li>
                    <li>Respond to your inquiries and provide customer support</li>
                    <li>Improve our website and services based on your feedback</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p>
                    We may share your information in the following situations:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>By Law or to Protect Rights:</strong> If required by law or if we believe in good faith that disclosure is necessary</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with vendors who assist us in operating our website and conducting our business</li>
                    <li><strong>Business Transfer:</strong> If 3D Scan Pro is involved in a merger, acquisition, or sale of assets</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or electronic storage is 100% secure.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p>
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p class="ml-4">
                    <strong>Email:</strong> privacy@yourdomain.com<br>
                    <strong>Address:</strong> Your Company Address
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Changes to This Privacy Policy</h2>
                <p>
                    We may update this Privacy Policy from time to time to reflect changes in our practices or for other operational, legal, or regulatory reasons. We will notify you of any material changes by updating the date of this Privacy Policy.
                </p>
                <p class="text-sm text-gray-600 mt-4">
                    <strong>Last Updated:</strong> January 2025
                </p>
            </section>
        </div>
    </main>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-6">
                        <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-blue-700 rounded-lg flex items-center justify-center">
                            <i class="fas fa-cube text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">3D Scan Pro</span>
                    </div>
                    <p class="text-gray-400 leading-relaxed">
                        Transforming the way professionals capture, analyze, and act on spatial data.
                    </p>
                </div>

                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Company</h3>
                    <ul class="space-y-3">
                        <li><a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About</a></li>
                        <li><a href="mailto:sales@yourdomain.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact</a></li>
                    </ul>
                </div>

                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Legal</h3>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>

                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Connect</h3>
                    <div class="flex space-x-4">
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
                            <i class="fab fa-linkedin text-gray-400 hover:text-white"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
                            <i class="fab fa-twitter text-gray-400 hover:text-white"></i>
                        </a>
                    </div>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 3D Scan Pro. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- JavaScript (Mobile Menu) -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });

                const mobileMenuLinks = mobileMenu.querySelectorAll('a');
                mobileMenuLinks.forEach(link => {
                    link.addEventListener('click', () => {
                        mobileMenu.classList.add('hidden');
                        const icon = mobileMenuButton.querySelector('i');
                        if (icon) {
                            icon.classList.remove('fa-times');
                            icon.classList.add('fa-bars');
                        }
                    });
                });
            }
        });
    </script>
</body>
</html>
```

#### Step 3: Customize the Privacy Policy

Update these sections with your actual information:

1. **Email address** (search for `privacy@yourdomain.com`):
   ```html
   <strong>Email:</strong> privacy@yourdomain.com
   ```
   Change to:
   ```html
   <strong>Email:</strong> your-email@yourdomain.com
   ```

2. **Company address**:
   ```html
   <strong>Address:</strong> Your Company Address
   ```
   Change to:
   ```html
   <strong>Address:</strong> 123 Main Street, City, State 12345
   ```

3. **Last updated date** (search for "January 2025"):
   ```html
   <strong>Last Updated:</strong> January 2025
   ```
   Change to today's date

4. **Add more sections** if needed (GDPR, CCPA, cookies, etc.)

---

### 3.4 Creating the Terms of Service Page

#### Step 1: Create a New File

1. Create a new file
2. Save it as `terms.html` in the same folder as `index.html`

#### Step 2: Add the Basic Structure

Copy this template into your `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for 3D Scan Pro">
    <title>Terms of Service | 3D Scan Pro</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-800 rounded-lg flex items-center justify-center">
                    <i class="fas fa-cube text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-gray-900">3D Scan Pro</span>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 font-medium transition-colors duration-300 hover:text-blue-600">Home</a>
                <a href="index.html#features" class="text-gray-700 font-medium transition-colors duration-300 hover:text-blue-600">Features</a>
                <a href="index.html#about" class="text-gray-700 font-medium transition-colors duration-300 hover:text-blue-600">About</a>
                <a href="mailto:sales@yourdomain.com" class="px-8 py-4 bg-blue-600 text-white font-semibold rounded-lg transition-all duration-300 hover:bg-blue-700 cursor-pointer">Contact</a>
            </div>
            
            <button class="mobile-menu-button md:hidden p-2 rounded-lg hover:bg-gray-100 transition-colors duration-300">
                <i class="fas fa-bars text-gray-900 text-xl"></i>
            </button>
            
            <div class="mobile-menu hidden absolute top-full left-0 right-0 bg-white shadow-lg md:hidden">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col space-y-4">
                    <a href="index.html" class="text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-blue-600">Home</a>
                    <a href="index.html#features" class="text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-blue-600">Features</a>
                    <a href="index.html#about" class="text-gray-700 font-medium py-2 transition-colors duration-300 hover:text-blue-600">About</a>
                    <a href="mailto:sales@yourdomain.com" class="px-8 py-4 bg-blue-600 text-white font-semibold rounded-lg transition-all duration-300 hover:bg-blue-700 cursor-pointer text-center">Contact</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 sm:py-24">
        <h1 class="text-4xl sm:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg max-w-none text-gray-700 space-y-8">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on 3D Scan Pro's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
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
                <p>
                    The materials on 3D Scan Pro's website are provided on an 'as is' basis. 3D Scan Pro makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>
                    In no event shall 3D Scan Pro or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on 3D Scan Pro's website, even if 3D Scan Pro or an authorized representative has been notified orally or in writing of the possibility of such damage.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on 3D Scan Pro's website could include technical, typographical, or photographic errors. 3D Scan Pro does not warrant that any of the materials on its website are accurate, complete, or current. 3D Scan Pro may make changes to the materials contained on its website at any time without notice.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>
                    3D Scan Pro has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by 3D Scan Pro of the site. Use of any such linked website is at the user's own risk.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>
                    3D Scan Pro may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of [Your State/Country], and you irrevocably submit to the exclusive jurisdiction of the courts located in [Your State/Country].
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Information</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="ml-4">
                    <strong>Email:</strong> legal@yourdomain.com<br>
                    <strong>Address:</strong> Your Company Address
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">10. Changes to Terms</h2>
                <p>
                    We reserve the right to modify these terms at any time. Changes will be effective immediately upon posting to the website. Your continued use of the website following any such modification constitutes your acceptance of the modified terms.
                </p>
                <p class="text-sm text-gray-600 mt-4">
                    <strong>Last Updated:</strong> January 2025
                </p>
            </section>
        </div>
    </main>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-6">
                        <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-blue-700 rounded-lg flex items-center justify-center">
                            <i class="fas fa-cube text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">3D Scan Pro</span>
                    </div>
                    <p class="text-gray-400 leading-relaxed">
                        Transforming the way professionals capture, analyze, and act on spatial data.
                    </p>
                </div>

                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Company</h3>
                    <ul class="space-y-3">
                        <li><a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About</a></li>
                        <li><a href="mailto:sales@yourdomain.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact</a></li>
                    </ul>
                </div>

                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Legal</h3>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>

                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Connect</h3>
                    <div class="flex space-x-4">
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
                            <i class="fab fa-linkedin text-gray-400 hover:text-white"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center hover:bg-blue-600 transition-colors duration-300">
                            <i class="fab fa-twitter text-gray-400 hover:text-white"></i>
                        </a>
                    </div>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 3D Scan Pro. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <!-- JavaScript (Mobile Menu) -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });

                const mobileMenuLinks = mobileMenu.querySelectorAll('a');
                mobileMenuLinks.forEach(link => {
                    link.addEventListener('click', () => {
                        mobileMenu.classList.add('hidden');
                        const icon = mobileMenuButton.querySelector('i');
                        if (icon) {
                            icon.classList.remove('fa-times');
                            icon.classList.add('fa-bars');
                        }
                    });
                });
            }
        });
    </script>
</body>
</html>
```

#### Step 3: Customize the Terms of Service

Update these sections with your actual information:

1. **Governing Law** (search for "[Your State/Country]"):
   ```html
   These terms and conditions are governed by and construed in accordance with the laws of [Your State/Country], and you irrevocably submit to the exclusive jurisdiction of the courts located in [Your State/Country].
   ```
   Change to:
   ```html
   These terms and conditions are governed by and construed in accordance with the laws of California, and you irrevocably submit to the exclusive jurisdiction of the courts located in California.
   ```

2. **Contact Email**:
   ```html
   <strong>Email:</strong> legal@yourdomain.com
   ```
   Change to:
   ```html
   <strong>Email:</strong> legal@yourdomain.com
   ```

3. **Company Address**:
   ```html
   <strong>Address:</strong> Your Company Address
   ```
   Change to:
   ```html
   <strong>Address:</strong> 123 Main Street, City, State 12345
   ```

4. **Last Updated Date**:
   ```html
   <strong>Last Updated:</strong> January 2025
   ```
   Change to today's date

---

### 3.5 Verifying the Links Work

After creating both files, verify that all links are working:

#### Test from index.html

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" link
4. You should see the privacy page
5. Click on "Terms of Service" link
6. You should see the terms page

#### Test from Privacy/Terms Pages

1. On the privacy or terms page, click the "Home" link in the header
2. You should return to `index.html`
3. Click the logo to return to the home page

#### Test Internal Links

1. On privacy/terms pages, click "Features" in the header
2. The page should scroll to the features section on the home page

**If links don't work**, check:
- File names match exactly: `privacy.html`, `terms.html`, `index.html`
- All files are in the same folder
- Links use correct case (lowercase)
- You saved all files after making changes

---

### 3.6 Complete Checklist for Legal Pages

- [ ] Created `privacy.html` file
- [ ] Created `terms.html` file
- [ ] Updated email addresses in both files
- [ ] Updated company address in both files
- [ ] Updated "Last Updated" dates
- [ ] Tested links from `index.html` to both pages
- [ ] Tested "Home" link from legal pages back to `index.html`
- [ ] Tested internal navigation links work from legal pages

---

## Troubleshooting Guide

### Issue 1: Links Don't Work

**Problem**: You click a link and nothing happens or you get a "404 Not Found" error.

**Solution**:

1. **Check the file exists**:
   - Make sure `privacy.html` and `terms.html` are in the same folder as `index.html`
   - Check the file names are spelled correctly (lowercase, with `.html` extension)

2. **Check the href is correct**:
   - Open `index.html` in your text editor
   - Search for the link (e.g., `privacy.html`)
   - Make sure it says `href="privacy.html"` (not `href="privacy.HTML"` or `href="privacy"`)

3. **Clear your browser cache**:
   - If you recently changed a link, your browser might be showing the old version
   - Press Ctrl+Shift+Delete (or Cmd+Shift+Delete on Mac) to clear cache
   - Close and reopen your browser

---

### Issue 2: Email Links Don't Work

**Problem**: You click an email link and nothing happens.

**Solution**:

1. **Check the email format**:
   - Make sure it says `mailto:` (not `mail:` or `email:`)
   - Example: `<a href="mailto:your-email@yourdomain.com">`

2. **Check you have a default email client**:
   - Your computer needs an email program set up (Gmail, Outlook, Apple Mail, etc.)
   - If you don't have one, the link won't work

3. **Test in a different browser**:
   - Try clicking the link in Chrome, Firefox, or Safari
   - If it works in one but not another, it's a browser configuration issue

---

### Issue 3: Page Layout Looks Broken

**Problem**: The page looks messy, text is overlapping, or buttons are in weird places.

**Solution**:

1. **Check Tailwind classes weren't accidentally deleted**:
   - Open your file in a text editor
   - Search for `class="btn-primary"` or `class="feature-card"`
   - Make sure the class names are complete and not broken

2. **Verify no HTML tags were accidentally deleted**:
   - Check that opening `<div>` tags have closing `</div>` tags
   - Look for unmatched `<p>` tags without `</p>` closing tags

3. **Reload the page**:
   - Press Ctrl+F5 (or Cmd+Shift+R on Mac) to do a hard refresh
   - This clears the browser cache and reloads the page fresh

---

### Issue 4: Text Formatting Looks Wrong

**Problem**: Text isn't bold, isn't the right size, or has wrong colors.

**Solution**:

1. **Check Tailwind classes are intact**:
   - Example: `<h1 class="text-4xl font-bold text-gray-900">`
   - Make sure you didn't accidentally remove `font-bold` or change `text-4xl`

2. **Check you didn't break the HTML**:
   - Make sure you have opening and closing tags: `<h1>...</h1>`
   - Check that class names are in quotes: `class="..."`

3. **Verify the color class name is correct**:
   - Tailwind uses specific color names: `blue-600`, `gray-900`, `green-500`
   - Make sure you didn't type `blue-color` or `darkgray` (wrong)

---

### Issue 5: Mobile Menu Doesn't Work

**Problem**: On mobile devices, clicking the hamburger menu doesn't open the menu.

**Solution**:

1. **Check the JavaScript is intact**:
   - Scroll to the bottom of your `index.html`
   - Look for the `<script>` section
   - Make sure you didn't accidentally delete any code

2. **Check you didn't break the HTML structure**:
   - Look for: `<button class="mobile-menu-button">`
   - Look for: `<div class="mobile-menu">`
   - Both should exist and be inside the `<header>` tag

3. **Test in a real mobile browser**:
   - Don't just resize your desktop browser
   - Use an actual mobile phone or use browser developer tools (F12) to test

---

### Issue 6: Images or Icons Don't Show

**Problem**: You see broken image icons instead of Font Awesome icons.

**Solution**:

1. **Check the Font Awesome link is in the `<head>`**:
   - Look for: `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">`
   - This should be in the `<head>` section of your HTML
   - Don't remove or modify this line

2. **Check your internet connection**:
   - Font Awesome icons are loaded from the internet
   - If you're offline, icons won't show
   - This is normal and will fix when you go online

3. **Check the icon class name is correct**:
   - Example: `<i class="fas fa-cube"></i>`
   - Make sure it says `fas` (not `fa` alone)
   - Check the icon name is correct (e.g., `fa-cube`, not `fa-cubes`)

---

### Issue 7: Colors Look Different Than Expected

**Problem**: You changed a color class but the page doesn't look different.

**Solution**:

1. **Check you're using the right Tailwind color name**:
   - For backgrounds: `bg-blue-600` (not `bg-blue`)
   - For text: `text-blue-600` (not `text-blue`)
   - Numbers matter: `blue-500` is different from `blue-600`

2. **Make sure you're editing the right element**:
   - Search for the text you want to change
   - Make sure you're changing the `class` attribute, not something else

3. **Clear your browser cache**:
   - Press Ctrl+Shift+Delete to clear cache
   - Reload the page

---

### Issue 8: Links Point to Wrong Pages

**Problem**: You click a link and it goes to the wrong place.

**Solution**:

1. **Check the href value**:
   - Right-click the link
   - Select "Inspect" or "Inspect Element"
   - Look at the `href` attribute
   - Make sure it matches where you want it to go

2. **Verify the file exists**:
   - If the link points to `privacy.html`, make sure that file exists
   - Check the file is in the same folder as `index.html`

3. **Check for typos**:
   - `privacy.html` ≠ `privacyhtml` (missing dot)
   - `terms.html` ≠ `term.html` (wrong name)
   - URLs are case-sensitive: `Privacy.html` ≠ `privacy.html`

---

## Best Practices

### 1. Always Backup Before Making Changes

Before editing your files, create a copy:
- Copy `index.html` to `index.html.backup`
- If something goes wrong, you can restore the original

### 2. Make Changes in Small Steps

Don't change everything at once:
1. Change one section (like the headline)
2. Save the file
3. Test it in your browser
4. Move to the next section

This way, if something breaks, you know exactly what caused it.

### 3. Use a Good Text Editor

Recommended free text editors:
- **VS Code** (Visual Studio Code) - Best option, free
- **Sublime Text** - Lightweight and fast
- **Notepad++** (Windows only)
- **Atom** - Good for beginners

**Avoid**: Microsoft Word, Google Docs, or other word processors (they add extra formatting that breaks HTML)

### 4. Test on Multiple Devices

Your page should work on:
- Desktop computers (Chrome, Firefox, Safari, Edge)
- Tablets (iPad, Android tablets)
- Mobile phones (iPhone, Android phones)

Use browser developer tools (F12) to test different screen sizes.

### 5. Keep Your Links Updated

Every time you create a new page, update the navigation links:
- Add links to the header menu
- Add links to the footer
- Test that all links work

### 6. Use Consistent Naming

Keep file names consistent:
- Use lowercase: `privacy.html` (not `Privacy.html`)
- Use hyphens for multi-word names: `privacy-policy.html` (not `privacy_policy.html`)
- Avoid spaces in file names

### 7. Document Your Changes

Keep a simple log of what you've changed:
```
2025-01-15: Updated company name to CloudScan Solutions
2025-01-16: Fixed broken demo links
2025-01-17: Created privacy and terms pages
```

This helps you remember what you've done and makes it easier to revert changes if needed.

### 8. Validate Your HTML

Use the free W3C HTML Validator:
1. Go to https://validator.w3.org/
2. Upload your HTML file
3. It will tell you if there are any errors

### 9. Keep Responsive Design in Mind

When updating text or adding content:
- Keep headlines concise (they need to fit on mobile)
- Test on mobile devices frequently
- Don't remove responsive classes like `sm:text-5xl` or `md:grid-cols-2`

### 10. Regular Updates

Plan to review and update your page:
- Update testimonials every quarter
- Refresh statistics annually
- Keep contact information current
- Update the "Last Updated" date on legal pages

---

## Quick Reference: Common Tasks

### Update Your Email Address

**Find and replace**:
- Search for: `iainhmunro@gmail.com`
- Replace with: `your-email@yourdomain.com`
- Locations: Lines 84, 498, and any custom pages

### Update Company Name

**Find and replace**:
- Search for: `3D Scan Pro`
- Replace with: `Your Company Name`
- Locations: Header (line 72), Footer (line 556), and title tags

### Add a New Feature Card

1. Find an existing feature card (lines 167-189)
2. Copy the entire `<div class="feature-card">...</div>` block
3. Paste it after the last feature card
4. Update the icon, title, description, and bullet points
5. Test that it displays correctly

### Change Color Scheme

1. Search for `bg-blue-600` to find all blue backgrounds
2. Replace with your color: `bg-green-600`, `bg-purple-600`, etc.
3. Do the same for `text-blue-600` (text colors)
4. Test on multiple devices

### Add a New Testimonial

1. Find an existing testimonial (lines 368-387)
2. Copy the entire `<div class="testimonial-card">...</div>` block
3. Paste it after the last testimonial
4. Update the star rating, quote, name, and title
5. Test that it displays correctly

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing the 3D Scan Pro landing page. Remember:

- **Start small**: Make one change at a time
- **Test often**: Check your work in a browser after each change
- **Backup regularly**: Keep copies of working versions
- **Ask for help**: If you're stuck, check this guide or search online for your specific error

Good luck with your landing page! If you need to make more complex changes in the future, consider learning more about HTML and CSS, or hire a web developer to help.