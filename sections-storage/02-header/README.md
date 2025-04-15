# Header Section

A fully responsive and customizable header section for Shopify themes, featuring a logo, navigation menu, search functionality, and cart integration.

## Features

- Responsive design with mobile menu
- Customizable logo with adjustable width
- Dynamic navigation menu support
- Search functionality with toggle
- Shopping cart integration with item count
- Account access link
- Sticky header option
- Dropdown menus for navigation items
- Mobile-friendly hamburger menu

## Dependencies

- Bootstrap Grid System (for layout)
- Custom icon set (for UI elements)
- JavaScript for interactive features

## Section Settings

### Logo Settings

| Setting | Type | Description | Default |
|---------|------|-------------|---------|
| Logo | Image Picker | Upload store logo | None |
| Logo Width | Range (50-250px) | Adjust logo size | 140px |

### Layout Settings

| Setting | Type | Description | Default |
|---------|------|-------------|---------|
| Sticky Header | Checkbox | Enable sticky positioning | True |
| Show Search | Checkbox | Display search functionality | True |
| Show Cart | Checkbox | Display shopping cart | True |

### Menu Block Settings

| Setting | Type | Description | Default |
|---------|------|-------------|---------|
| Menu | Link List | Select navigation menu | main-menu |

## Usage

1. Add the "Header" section through the Theme Editor
2. Configure logo and layout settings
3. Set up navigation menu:
   - Create menu items in Shopify admin
   - Add dropdown items if needed
   - Select menu in theme settings
4. Customize appearance:
   - Adjust logo size
   - Toggle features (search, cart)
   - Enable/disable sticky header

## Features Breakdown

### 1. Logo
- Supports image upload
- Fallback to store name
- Responsive sizing
- Customizable width

### 2. Navigation
- Multi-level dropdown support
- Mobile-friendly collapse
- Dynamic menu from Shopify
- Hover effects

### 3. Search
- Toggle functionality
- Full-width search bar
- Close button
- Mobile optimization

### 4. Shopping Cart
- Real-time item count
- Direct link to cart page
- Visual indicator

### 5. Mobile Menu
- Hamburger toggle
- Collapsible navigation
- Touch-friendly
- Smooth transitions

## Best Practices

1. **Logo**
   - Use SVG format when possible
   - Maintain aspect ratio
   - Consider mobile visibility
   - Optimize file size

2. **Navigation**
   - Limit main menu items
   - Use clear labels
   - Group similar items
   - Consider touch targets

3. **Mobile Experience**
   - Test all breakpoints
   - Ensure tap targets are large enough
   - Maintain readability
   - Check load times

## Customization

Key CSS classes for styling:

```css
.site-header /* Main header container */
.header-logo /* Logo container */
.site-nav /* Navigation wrapper */
.main-menu /* Primary menu list */
.submenu /* Dropdown menu */
.header-actions /* Icons/cart area */
.search-container /* Search form */
```

## JavaScript Features

1. **Mobile Menu Toggle**
   - Shows/hides navigation on mobile
   - Manages aria states
   - Handles transitions

2. **Search Functionality**
   - Toggle search panel
   - Focus management
   - Close on outside click

## Troubleshooting

1. **Navigation Issues:**
   - Check menu configuration in Shopify admin
   - Verify link list assignment
   - Test dropdown functionality
   - Check mobile menu behavior

2. **Search Problems:**
   - Verify search route configuration
   - Check JavaScript console
   - Test form submission
   - Verify toggle functionality

3. **Responsive Behavior:**
   - Test different screen sizes
   - Check breakpoint transitions
   - Verify sticky header
   - Test mobile menu

4. **Cart Integration:**
   - Verify cart routes
   - Check item count updates
   - Test cart link functionality
   - Verify AJAX updates

## Version History

- 1.0.0: Initial release
- 1.0.1: Added sticky header option
- 1.0.2: Enhanced mobile menu
- 1.0.3: Improved search functionality
- 1.0.4: Added dropdown animations
- 1.0.5: Accessibility improvements 