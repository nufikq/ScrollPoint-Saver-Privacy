# Privacy Policy for ScrollPoint Saver

**Last Updated**: August 6, 2025

## Overview
ScrollPoint Saver is designed with privacy as a core principle. This extension helps users save and restore scroll positions on web pages while keeping all data completely local to their device.

## Single Purpose
This extension serves one specific purpose: to save and restore scroll positions on web pages. Users can bookmark specific scroll locations on any webpage and quickly return to those positions later.

## Data Collection and Storage

### What Data We Collect Locally:
1. **Scroll Positions**: The vertical scroll position (scrollTop values) of scrollable elements on web pages
2. **Page URLs**: Website URLs where scroll points are saved (using `window.location.href`)
3. **Element Selectors**: CSS selectors to identify scrollable elements on pages (generated via DOM traversal)
4. **Custom Names**: User-provided names for saved scroll points

### What Data We DO NOT Collect:
- Personal information (names, emails, addresses)
- Browsing history beyond scroll point URLs
- Content of web pages
- User credentials or authentication data
- Financial information
- Location data
- Communications or messages

### How Data is Stored:
- All data is stored locally using Chrome's `chrome.storage` API
- No data is transmitted to external servers or third parties
- Data persists only on your local device
- No remote servers or databases are used

## Technical Implementation Details

### DOM Interaction:
- The extension scans web pages for scrollable elements using `document.querySelectorAll('*')`
- It checks CSS properties (`overflow`, `overflowY`) to identify scrollable containers
- Element selectors are generated using tag names and DOM hierarchy for later identification

### Data Processing:
- Scroll positions are captured using `element.scrollTop` property
- Element identification uses CSS selectors (IDs, tag names, nth-child selectors)
- All processing happens locally in your browser

## Permissions Justification

### Storage Permission
**Purpose**: Save scroll point data locally
**Usage**: Stores scroll positions, URLs, and user-defined names using Chrome's local storage

### ActiveTab Permission  
**Purpose**: Access the currently active tab
**Usage**: Read scroll positions and inject navigation buttons on the current webpage

### Scripting Permission
**Purpose**: Inject content scripts into web pages
**Usage**: Execute code to detect scrollable elements, save positions, and create navigation buttons

### Host Permission (*://*/*)
**Purpose**: Work on all websites
**Usage**: Allow users to save scroll points on any website they visit without manual site-by-site permission

## Data Usage and Sharing

### Local Processing Only:
- All scroll position calculations happen in your browser
- Element detection and selector generation occur locally
- No analytics or tracking data is collected

### No Data Sharing:
- Zero data transmission to external servers
- No third-party integrations or data sharing
- No advertising or marketing use of data
- No user profiling or behavioral analysis

## Data Retention and Control

### User Control:
- Users can delete individual scroll points through the extension interface
- Users can delete all scroll points at once
- Users can toggle visibility of scroll point buttons
- Uninstalling the extension removes all stored data

### Data Persistence:
- Data persists between browser sessions until manually deleted
- Data is tied to your Chrome profile and doesn't sync across devices
- No automatic data backup or cloud storage

## Security Measures

### Local Security:
- Data is protected by Chrome's built-in storage security
- No network transmission means no interception risk
- No external authentication or API keys required

### Code Security:
- No remote code execution
- All functionality is contained within the extension package
- No external script loading or dynamic code evaluation

## Compliance Information

### Chrome Web Store Categories:
Based on this extension's functionality, the following data categories apply:

✅ **Web history**: URLs where scroll points are saved
✅ **User activity**: Scroll position data and user interactions with scroll points
✅ **Website content**: CSS selectors and DOM element identification

❌ **Not collected**: Personal information, health data, financial data, authentication data, communications, location data

## Contact Information
For questions about this privacy policy or data practices, please contact [your contact information].

## Policy Updates
This privacy policy may be updated to reflect changes in the extension's functionality. Users will be notified of material changes through the Chrome Web Store update process.

---

**Summary**: This extension operates entirely locally, stores only scroll-related data, and never transmits information to external servers. Your privacy and data remain completely under your control.
