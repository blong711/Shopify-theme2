# Header Section

This Liquid corresponds to this HTML.

Path to HTML: sections-storage/02-header/header.html
Path to Liquid: sections-storage/02-header/header.liquid

## Section Overview
The header section is the main navigation area of the website. It contains:
- Mobile menu toggle
- Logo
- Main navigation menu with dropdowns
- Search functionality
- Account access
- Wishlist
- Shopping cart

## HTML to Liquid Conversion Details

### 1. Logo
- Converted static logo to dynamic using `section.settings.logo`
- Added fallback to shop name if no logo is set
- Used Shopify's image URL filter for proper image handling

### 2. Navigation Menu
- Converted static menu to dynamic using `linklists[section.settings.menu].links`
- Implemented dropdown menu support with `link.links`
- Added conditional rendering for dropdown arrows
- Converted mega menu to use dynamic content from child links

### 3. Search Functionality
- Integrated with Shopify's search route
- Added dynamic placeholder text
- Maintained the existing search UI while making it functional

### 4. Account & Cart
- Connected account link to Shopify's account route
- Added dynamic cart count using `cart.item_count`
- Connected wishlist to a dedicated page
- Maintained existing UI elements while making them functional

### 5. Schema Settings
Added the following settings:
- Logo picker
- Menu selector
- Search placeholder text
- Cart count toggle
- Wishlist visibility toggle

## Usage
This section should be placed in the theme's header area, typically in the `layout/theme.liquid` file. It provides the main navigation and essential e-commerce functionality for the store.

## Notes
- The mega menu dropdown uses child links' featured images if available
- New labels can be added through metafields
- The search functionality uses Shopify's built-in search
- Cart count updates automatically through Shopify's cart object 