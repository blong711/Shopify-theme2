# Top Bar Section

This Liquid corresponds to this HTML.

Path to HTML: sections-storage/01-topbar/topbar.html
Path to Liquid: sections-storage/01-topbar/topbar.liquid

## Section Overview
The top bar section is a horizontal bar that appears at the very top of the website. It contains:
- Social media icons (Facebook, Instagram, Twitter, Snapchat)
- An announcement marquee with customizable messages
- Language and currency selectors

## HTML to Liquid Conversion Details

### 1. Social Media Icons
- Converted static social media links to dynamic settings
- Added conditional rendering with `{% if section.settings.show_social_icons %}`
- Each social media URL is now configurable through theme settings
- Added individual URL settings for each social platform

### 2. Announcement Bar
- Converted static announcement text to dynamic blocks
- Implemented a block system for multiple announcements
- Added a toggle to show/hide the announcement bar
- Created a preset with default announcements

### 3. Language & Currency Selectors
- Replaced static selectors with Shopify's built-in localization selectors
- Added toggles to show/hide language and currency selectors
- Used `{{ localization.language.selector }}` and `{{ localization.country.selector }}` for dynamic selection

### 4. Schema Settings
Added the following settings:
- Social Media section with URL inputs and visibility toggle
- Announcement section with block system for messages
- Language & Currency section with visibility toggles

## Usage
This section should be placed at the top of the theme, typically in the `layout/theme.liquid` file. It provides a flexible way to display important information and navigation elements at the top of the website. 