 # Shopify Dev Store


[<img src="src/assets/images/devworthy_amiresponsive_whole.png" alt="An image representing how the site looks across different devices of varying size.">](https://anthonyradose.github.io/dev-worthy/#/)


By Krishan G


[🔗 View the live project here.](https://krish-demostore.myshopify.com/)


This is the documentation for my demo Shopify store – an urban clothing brand using the Horizon theme and enhanced with custom features to improve user experience and merchant KPIs.
I have demostared how to apply these features using platform configuration as well as code development. I hope you enjoy it.


# **Contents**
- [User Experience](#user-experience)
- [Special Features](#features)
    * [Homepage Video Banner](#homepage-video-banner)
    * [Metafield Custom Product Attribute](#metafield-custom-product-attribute)
    * [Bootstrap Theme](#bootstrap-theme)
        + [Bootstrap Toasts - Alert Messages](#)
        + [Bootstrap Carousel - USP (Unique Selling Points)](#)
    * [Guest Checkout](#guest-checkout)
    * [Product Reviews](#product-reviews)
    * [Shipping Logic](#shipping-logic)
    * [Sort By Filter](#sort-by-filter)
    * [404 Page](#404-page)
- [SEO Optimisation](#seo-optimisation)
    * [Internal and External Links and SEO](#internal-and-external-links-and-seo)
    * [Sitemap XML](#sitemap-xml)
    * [Robots.txt](#robotstxt)
    * [Keyword Research](#keyword-research)
- [Code Validation](#code-validation)
        + [CSS Validation](#css-validation)
        + [HTML Validation](#html-validation)
        + [Javascript Validation](#javascript-validation)
        + [Python Validation](#python-validation)
- [Performance](#performance)
        + [Google Lighthouse Score](#google-lighthouse-score)
        + [Microsoft Edge Lighthouse score](#microsoft-edge-lighthouse-score)
- [Bugs Encountered during Testing](#bugs-encountered-during-testing)
        + [Bug 1](#bug-1)
        + [Bug 2](#bug-2)
        + [Bug 3](#bug-3)
        + [Bug 4](#bug-4)
- [Accessibility](#accessibility)
- [Technologies used](#technologies-used)
    * [Languages](#languages)
    * [Frameworks and libraries](#frameworks-and-libraries)
    * [Databases](#databases)
    * [Other tools](#other-tools)
- [Credits and Borrowed Resources](#credits-and-borrowed-resources)
    * [BootStrap Support](#bootstrap-support)
    * [Project Support](#project-support)
    * [E-commerce User Stories Support](#e-commerce-user-stories-support)
    * [Static Content and Copy](#static-content-and-copy)
    * [Product Details and Images](#product-details-and-images)
    * [Mind Map images](#mind-map-images)
    * [Web and Social Media Marketing](#web-and-social-media-marketing)
 


# User Experience
I selected the Horizon theme as the foundation for my demo store because it strikes a powerful balance between clean minimalism and conversion-focused features. It gives me enough flexibility to showcase my core understanding of shopify and knowledge of what an e-commerce store needs today.

# Features

## Homepage Video Banner
[![Shopify Compatible](https://img.shields.io/badge/Shopify-Compatible-green.svg)](https://www.shopify.com/)
[![Liquid](https://img.shields.io/badge/Liquid-Template-blue.svg)](https://shopify.github.io/liquid/)
[![Responsive](https://img.shields.io/badge/Design-Responsive-orange.svg)](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)

> A custom Shopify Liquid section that creates a fullwidth video banner with autoplay functionality and customizable overlay content.

### ✨ Features

- 🎬 **Fullwidth video background** with autoplay, muted, and looped playback
- 🎨 **Customizable overlay** with adjustable opacity
- 🏷️ **Dynamic logo display** with size controls and optional white filter
- ✏️ **Editable text content** with typography controls (title and subtitle)
- 🔘 **Call-to-action button** with multiple styling options
- 📱 **Fully responsive** design optimized for mobile devices
- ✨ **Professional animations** with hover effects and smooth transitions

### 📦 Installation

1. In your Shopify admin, navigate to **Online Store > Themes**
2. Click **Actions > Edit code** on your active theme
3. In the **Sections** folder, click **Add a new section**
4. Name the file `video-banner.liquid`
5. Copy and paste the provided code into the file
6. Click **Save**

### 🚀 Usage

### Adding to Templates

Add the section to any template file using:
```liquid
{% section 'video-banner' %}
```

### 🎥 Video Setup

1. Upload your video file to **Settings > Files** in Shopify admin
2. Copy the file URL from the Files section
3. In the theme customizer, navigate to the Video Banner section
4. Paste the video URL in the "Video URL" field
5. Optionally add a poster image for faster loading

### ⚙️ Customization Options

The section includes comprehensive customization options accessible through the Shopify theme editor:

#### 🎬 Video Settings
- **Video URL**: Direct link to your uploaded video file
- **Video Poster Image**: Fallback image displayed before video loads

#### 🎨 Overlay Settings
- **Overlay Opacity**: Control background darkening (0-80%)
- **Text Color**: Set color for all overlay text

#### 🏷️ Logo Settings
- **Logo Upload**: Add your brand logo
- **Logo Width**: Control logo size (100-400px)
- **Convert to White**: Apply white filter for dark logos

#### ✏️ Text Settings
- **Title**: Main heading text
- **Title Font Size**: Typography control (24-72px)
- **Title Font Weight**: Choose from Light to Bold
- **Subtitle**: Supporting description text
- **Subtitle Font Size**: Typography control (14-24px)

#### 🔘 Button Settings
- **Button Text**: Call-to-action text
- **Button Link**: Destination URL
- **Button Style**: Choose between Filled or Outline
- **Button Color**: Background/border color
- **Button Text Color**: Text color for filled buttons
- **Button Font Size**: Typography control (12-20px)

## 🏗️ Technical Implementation

### File Structure
```
sections/
└── video-banner.liquid    # Main section file with Liquid, CSS, and Schema
```

### Code Architecture

The section consists of three main components:

1. **CSS Styles**: Embedded styles for layout, responsiveness, and animations
2. **HTML Structure**: Liquid template with video element and overlay content
3. **Schema Configuration**: JSON schema defining all customizable settings

### 📱 Responsive Design

The section automatically adapts to different screen sizes:
- **Desktop**: Full viewport height (100vh) with large typography
- **Mobile**: Reduced height (70vh) with scaled-down text and logo sizes

## 🛠️ Troubleshooting

### ❌ Common Issues and Solutions

#### Liquid Syntax Error: Unexpected character +

**Problem**: Shopify Liquid doesn't support the `+` operator for string concatenation.

```liquid
<!-- ❌ This causes an error -->
{{ section.settings.logo | img_url: section.settings.logo_width + 'x' }}
```

**Solution**: Use a fixed image size with CSS for scaling:

```liquid
<!-- ✅ This works correctly -->
{{ section.settings.logo | img_url: '400x' }}
<!-- Control size with CSS -->
style="max-width: {{ section.settings.logo_width }}px;"
```

**Why this happens**: Shopify Liquid uses different syntax than JavaScript. For string concatenation, use the `append` or `prepend` filters instead of `+`.

#### 🎥 Video Not Playing
- Ensure the video file is uploaded to Shopify Files
- Check that the video URL is correct and accessible
- Verify the video is in MP4 format for best browser compatibility
- Modern browsers require user interaction for autoplay with sound (this section uses muted autoplay)

#### ⚡ Performance Optimization
- Keep video files under 10MB for optimal loading
- Use poster images to improve perceived loading speed
- Consider using different video formats for different devices

## 🌐 Browser Compatibility

| Browser | Support | Notes |
|---------|---------|--------|
| Chrome | ✅ Full | Autoplay supported |
| Firefox | ✅ Full | Autoplay supported |
| Safari | ✅ Full | Autoplay supported |
| Edge | ✅ Full | Autoplay supported |
| Mobile Browsers | ✅ Full | Uses `playsinline` attribute |
| Older Browsers | ⚠️ Partial | Graceful fallback to poster image |

## 🔧 Development Notes

### Key Liquid Techniques Used
- `img_url` filter for responsive image sizing
- Conditional rendering with `{% if %}` statements
- Dynamic CSS properties using Liquid variables
- Schema-driven customization options

### CSS Features
- CSS Grid and Flexbox for layout
- Object-fit for video scaling
- CSS custom properties for dynamic styling
- Mobile-first responsive design
- Smooth transitions and hover effects

[Back to contents](#contents)


# Metafield Custom Product Attribute

## Overview

This documentation covers how to add custom product attributes using Shopify metafields and dynamic sources through the theme customizer - **no code editing required**.

## What Are Metafields?

Metafields are Shopify's way of storing custom data that doesn't fit into standard product fields. They allow you to add additional information like sustainability details, care instructions, sizing guides, or any other custom attributes to your products.

## Implementation Guide

### Prerequisites

- Shopify store with modern theme (Horizon, Dawn, etc.)
- Admin access to Shopify store
- Products to add custom attributes to

### Step 1: Create Metafield Definition

1. Navigate to **Shopify Admin** → **Settings** → **Metafields**
2. Click **"Add definition"**
3. Configure your metafield:

| Field | Value | Notes |
|-------|-------|-------|
| **Name** | `Sustainable Material` | Human-readable label shown in admin |
| **Namespace and key** | `custom.sustainable_material` | Technical identifier for the field |
| **Description** | `Information about sustainable materials used` | Optional helper text |
| **Type** | `Single line text` | Data type - see options below |
| **Content type** | `Products` | Where this metafield can be used |

4. Click **"Save"**

#### Available Data Types

- **Single line text** - Short text (e.g., "Made from sustainable cotton")
- **Multi-line text** - Longer text with line breaks
- **Rich text** - Formatted text with bold, italic, links
- **Number** - Numeric values
- **True/False** - Yes/no checkbox
- **Date** - Calendar dates
- **URL** - Web addresses
- **JSON** - Structured data

### Step 2: Add Content to Products

1. Go to **Products** in Shopify admin
2. **Edit** the product you want to add the attribute to
3. Scroll to the **"Metafields"** section (usually near the bottom)
4. Find your **"Sustainable Material"** field
5. Enter your content (e.g., `Made from sustainable cotton.`)
6. **Save** the product

> **Tip:** You can bulk-edit metafields using CSV export/import for multiple products.

### Step 3: Display via Theme Customizer

1. Navigate to **Online Store** → **Themes** → **Customize**
2. Go to a **product page** in the preview
3. Add a new section or block:
   - Look for **"Custom content"**, **"Rich text"**, or **"Text"** blocks
   - Or use existing **"Product information"** sections
4. In the block settings, find text fields that support dynamic sources
5. Click the **"Connect dynamic source"** icon (🔗 chain link or database symbol)
6. Select **"Products"** → **"Sustainable Material"** (your metafield name)
7. **Save** your changes

### Step 4: Style and Position

- Use the **theme customizer** to position your block appropriately
- Adjust **text styling** (font size, color, alignment) through customizer settings
- **Preview** your changes across different devices
- **Publish** when satisfied

## Best Practices

### Naming Conventions

- **Names**: Use clear, descriptive names (`Sustainable Material`, `Care Instructions`)
- **Keys**: Use lowercase with underscores (`sustainable_material`, `care_instructions`)
- **Namespaces**: Stick with `custom` for simplicity, or create logical groups (`eco`, `sizing`)

### Content Guidelines

- Keep text concise and customer-focused
- Use consistent formatting across products
- Only populate metafields for relevant products
- Consider multiple languages if you have international customers

### Organization

- Group related metafields with consistent naming
- Use descriptions to document the purpose of each metafield
- Consider creating a content style guide for team members

## Bulk Management

### CSV Method

1. **Export products** via CSV from Products → Export
2. Add column: `Metafield: custom.sustainable_material [single_line_text_field]`
3. Fill in values for applicable products
4. **Import** the updated CSV

### Shopify Flow (Plus only)

Create automation rules to populate metafields based on:
- Product tags
- Vendor information  
- Collection membership
- Other product attributes

## Troubleshooting

### Common Issues

| Problem | Solution |
|---------|----------|
| **Metafield not appearing in admin** | Check metafield definition is saved and content type is "Products" |
| **Dynamic source option missing** | Verify your theme supports dynamic sources (most modern themes do) |
| **Content not displaying** | Ensure metafield has content and dynamic source is properly connected |
| **Styling issues** | Use theme customizer styling options rather than custom CSS |

### Verification Steps

1. **Check metafield content** - Visit product admin page and verify field is populated
2. **Test dynamic source** - In customizer, verify the connection shows your metafield name
3. **Preview thoroughly** - Test on different products, including those without the metafield
4. **Mobile testing** - Ensure display works properly on mobile devices

## Advanced Usage

### Multiple Metafields

You can create multiple metafields for different attributes:
- `custom.sustainable_material` - "Made from organic cotton"
- `custom.care_instructions` - "Machine wash cold, tumble dry low"  
- `custom.sizing_notes` - "Runs small, consider sizing up"

### Conditional Display

Modern themes automatically handle conditional display - metafields only show when they contain content.

### Rich Content

For more complex content, consider:
- **Multi-line text** for longer descriptions
- **Rich text** for formatted content with links
- **URL fields** for linking to certificates or additional info

## Maintenance

### Regular Tasks

- **Review content** periodically for accuracy and consistency
- **Update styling** through theme customizer as needed
- **Monitor performance** - too many metafields can slow admin interface
- **Document changes** for team members

### When Updating Themes

- Metafield definitions persist through theme changes
- Dynamic source connections may need to be re-established
- Test display after theme updates

## Support Resources

- **Shopify Help Center** - Search for "metafields" 
- **Theme Documentation** - Check your theme's specific documentation
- **Shopify Community** - Developer and merchant forums
- **Theme Support** - Contact your theme developer if dynamic sources aren't available

---

**Last Updated:** September 2025  
**Compatible With:** Modern Shopify themes with dynamic source support
