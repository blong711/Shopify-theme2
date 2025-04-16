# Banner Countdown Section

This section displays a promotional banner with a countdown timer, typically used for sales or special events.

## Features

- Customizable banner image
- Configurable season text (e.g., "SUMMER SALE")
- Adjustable discount text (e.g., "50% OFF")
- Editable promo code
- Configurable countdown end date
- Customizable button text and link

## Schema Settings

1. **Banner Image**
   - Type: Image Picker
   - Description: The main promotional image for the banner

2. **Season Text**
   - Type: Text
   - Default: "SUMMER SALE"
   - Description: The seasonal or promotional text

3. **Discount Text**
   - Type: Text
   - Default: "50% OFF"
   - Description: The discount offer text

4. **Promo Code**
   - Type: Text
   - Default: "12D34E"
   - Description: The promotional code to be displayed

5. **Countdown End Date**
   - Type: Text
   - Format: YYYY-MM-DD HH:MM:SS
   - Default: "2024-12-31 23:59:59"
   - Description: The end date and time for the countdown timer

6. **Button Link**
   - Type: URL
   - Description: The destination URL for the "Shop Now" button

7. **Button Text**
   - Type: Text
   - Default: "Shop Now"
   - Description: The text displayed on the button

## Usage

1. Add the section to your theme
2. Upload a banner image
3. Configure the promotional text and discount information
4. Set the countdown end date
5. Add the button link and customize the button text

## Dependencies

- Requires JavaScript for countdown functionality
- Uses the `wg-countdown-2` class for countdown styling
- Implements `wow` animations for fade-in effects

## Notes

- The countdown timer uses the `js-countdown` class and requires JavaScript initialization
- The section is responsive and centered
- Animations are triggered using the `wow` library 