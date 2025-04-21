## Prompt for Cursor AI

Go through each file in this folder:  
`/home/ryotaru/Shopify-theme2/sections`

For every section file:

- Check if the section uses `"blocks"` in its schema.  
- If the section does **not** use `"blocks"`, update the section to use `blocks` to allow for more flexible content management.
- Preserve any existing settings by migrating them into block-level settings when appropriate.
- Use appropriate block types like `"text"`, `"image"`, `"product"`, `"collection"`, `"custom"` based on the content in the section.
- Make sure the `for` loop that outputs content is updated to iterate over `section.blocks` instead of static content where possible.
- Add `"limit": 5` or another reasonable value to `blocks` if needed.
- Ensure the structure follows Shopify's best practices for Online Store 2.0 compatibility.

Once done, ensure the updated section still renders correctly usinge dummy content or mock data.

✅ Bonus: Add comments in the code to show what was changed or upgraded.
