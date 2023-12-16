# Ryanair Website - Lighthouse Report

## Overview

I ran Lighthouse against the Ryanair homepage (https://www.ryanair.com/) to audit its performance, accessibility, best practices, and SEO. 

## Test Setup

- Tool: Lighthouse 11.0.0
- Emulated Device: Desktop 
- Network Throttling: Unknown
- Date: Dec 11, 2023

## Analysis

### Performance (Score: 35)

The Ryanair homepage has significant opportunities to improve performance, scoring only 35 in this category.

- The **First Contentful Paint** takes 4.5s, which is quite high. This can likely be improved by optimizing images, deferring non-critical JS/CSS, and minimizing main thread work.

- **Largest Contentful Paint** takes 8.5s to render which indicates noticeable load delays for users. This is likely due to large JavaScript bundles and unoptimized images.

- **Total Blocking Time** caused by main thread work is over 2s. Reducing JavaScript parse/compile time and execution would reduce this blocking time.

- 2 large non-lazy-loaded images contribute heavily to the LCP. Preloading or lazy-loading these could help improve LCP.

### Accessibility (Score: 88)

The site scores well in accessibility with a score of 88 but still has some areas for improvement:

- Some ARIA attributes do not have valid names/values. Fixing these would improve the experience for screen reader users.

- There are a few elements marked [aria-hidden=true] that contain focusable descendents. These descendents should be removed or disabled.

### Best Practices (Score: 95)

Best practices score is 95. The main issue is that several large first party JavaScript files are missing their source maps in production. Adding source maps would improve debugging capability and provide better insights.

### SEO (Score: 97)

With a score of 97, SEO best practices look good overall. 

- 70% of tap targets are sized appropriately. Some footer links should be increased for better usability.

- No major issues were found with structured data, metadata, headings, or other SEO fundamentals.

## Conclusion  

The major focus areas for Ryanair should be:

- Improving performance by optimizing images, JS/CSS delivery, and reducing main thread work
- Adding source maps to first party JS bundles
- Increasing tap target size for some footer links  
- Remediating invalid ARIA attributes and hidden focusable elements

This would help significantly improve user experience especially on mobile devices.
