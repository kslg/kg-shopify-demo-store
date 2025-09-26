 # Shopify Dev Store


[<img src="src/assets/images/devworthy_amiresponsive_whole.png" alt="An image representing how the site looks across different devices of varying size.">](https://anthonyradose.github.io/dev-worthy/#/)


By Krishan G


[🔗 View the live project here.](https://krish-demostore.myshopify.com/)


This is the documentation for my demo Shopify store – an urban clothing brand using the Horizon theme and enhanced with custom features to improve user experience and merchant KPIs.
I have demostared how to apply these features using platform configuration as well as code development. I hope you enjoy it.


# **Contents**
- [User Experience](#user-experience)
- [Features](#features)
    * [Homepage Video Banner](#homepage-video-banner)
    * [Order Confirmation Email](#order-confirmation-email)
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
I've used the Horizon themes which provides maximum flexibility, making editing easy and giving merchants powerful and intuitive tools. The theme is built on component-driven architecture and offer "total design freedom" with enhanced performance and intuitive visual editing capabilities.

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

