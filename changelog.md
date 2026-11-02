# Changelog — WEDE5020 Golden Crust Bakery

**Student:** Collins Shai  
**Student Number:** 10527696

## 19 September 2026 — Part 2 CSS and Responsive Design

### External CSS
- Created `css/style.css` as the single external stylesheet for all five website pages.
- Linked the stylesheet to `index.html`, `about.html`, `products.html`, `enquiry.html` and `contact.html`.
- Used a consistent naming convention and organised the stylesheet into sections for reset, layout, typography, components and responsive rules.

### Base styling
- Added a CSS reset to reduce browser-specific default spacing differences.
- Added global font, colour, background, line-height and box-sizing rules.
- Added reusable CSS variables for the Golden Crust brown, gold and cream palette.
- Added a maximum content width and responsive percentage-based container width.

### Typography
- Added a consistent sans-serif font stack.
- Added responsive heading sizes using `clamp()`.
- Added font weights, line-height and letter-spacing for headings and navigation.
- Added muted text styling for supporting information.

### Desktop layout
- Implemented CSS Grid for the home hero, value cards, products, contact cards and enquiry form.
- Implemented Flexbox for navigation, action buttons and footer layout.
- Added consistent spacing, borders, shadows and rounded cards.
- Added clear calls-to-action for product and enquiry journeys.

### Interaction styling
- Added `:hover` effects to navigation links, buttons and cards.
- Added `:focus-visible` states for keyboard accessibility.
- Added active navigation styling and `aria-current="page"` to identify the current page.

### Responsive design
- Added tablet breakpoint at 60rem.
- Added mobile breakpoint at 42rem.
- Converted major multi-column layouts to single-column layouts on small screens.
- Adjusted navigation, buttons, footer and form layout for mobile.
- Used relative units and fluid sizing to avoid fixed desktop-only layouts.

### Responsive images
- Added `picture`, `srcset` and `sizes` to the Home page hero image.
- Used the supplied `bakery-hero.svg` asset from the Part 1 project resources.

### Accessibility
- Added descriptive alt text.
- Added form labels and required attributes.
- Added visible keyboard focus states.
- Added reduced-motion support with `prefers-reduced-motion`.

### Documentation
- Added this changelog.
- Added a README documenting the CSS implementation, responsive breakpoints and testing process.


## 2 November 2026 — Part 3 functionality, forms and SEO

### Part 2 review and feedback status
- Reviewed all five existing HTML pages, the shared stylesheet and Part 2 documentation before extending the project.
- No lecturer feedback or Part 2 marking comments were supplied. No feedback items have therefore been fabricated; the following changes are independently identified Part 3 enhancements.
- Retained the existing Golden Crust Bakery name, five-page structure, colour palette and responsive CSS foundation.

### JavaScript and dynamic content
- Added `js/main.js` and loaded it with `defer` on all pages.
- Added a JavaScript-driven product catalogue with keyword search, category filtering, price/name sorting and a live result count.
- Added product-specific enquiry links that prefill the enquiry form.
- Added an accessible image lightbox using the native dialog element, including close button, backdrop handling and Escape-key support.
- Added reusable accordion interaction logic for accessible accordion controls.
- Added a Leaflet interactive map on the Contact page with approximate Pretoria Central and Menlyn area markers; labels clarify that these are illustrative areas, not verified shop addresses.

### Enquiry form
- Expanded the enquiry form with phone number, enquiry category, quantity, optional required date and a longer message field.
- Added client-side validation using native constraint validation and JavaScript feedback.
- Added an illustrative starting-price calculation for product/order/celebration enquiries and acknowledgements for volunteer/sponsorship/other enquiries.
- Added a disclaimer that estimates are not live quotations or availability checks.

### Contact form
- Added a separate general contact form requesting name, email, optional phone, message type and full message.
- Added validation and JavaScript compilation of the entered fields into a prefilled email using `mailto:`. The visitor must review and send the email in their own email application.
- Used a reserved `.example` recipient placeholder to avoid inventing a real organisation email; it must be replaced with an authorised recipient before live use.

### SEO, security and performance
- Added social sharing metadata, theme colour, favicon reference and robots directives to all pages.
- Added `robots.txt` and `sitemap.xml`; documented that the placeholder Netlify domain must be replaced after deployment.
- Added original SVG product illustrations, descriptive alt text and lazy loading for product images.
- Added map attribution, Leaflet Subresource Integrity attributes, HTTPS deployment guidance and advice not to expose secrets in client-side code.

### Documentation and deployment preparation
- Updated README with Part 3 implementation details, testing checklist, form limitations, SEO details and Netlify deployment steps.
- Updated references with MDN, Google Search Central, Leaflet, OpenStreetMap and Netlify documentation.
- Deployment and GitHub push remain user actions because they require the student's own account authentication.
