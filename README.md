# WEDE5020 Part 3 — Golden Crust Bakery

**Student:** Collins Shai  
**Student Number:** 10527696  
**Project:** Golden Crust Bakery (hypothetical Pretoria bakery concept)  
**Part:** Part 3 — Functionality, SEO, Forms and Deployment

## 1. Project overview
A five-page responsive website for a fictional neighbourhood bakery concept. Pages: `index.html`, `about.html`, `products.html`, `enquiry.html` and `contact.html`. The existing Part 2 visual identity (brown, gold and cream) and CSS layout have been retained and extended.

## 2. Part 3 functionality
- `js/main.js` builds the product catalogue from JavaScript data and implements live keyword search, category filtering, price/name sorting and a result count.
- Home page gallery uses a native HTML `<dialog>` lightbox with close button, backdrop click and descriptive alternative text.
- Product enquiry links prefill the enquiry form using a URL query parameter.
- Enquiry form validates name, email, phone, enquiry type, quantity, date and message. It displays an illustrative estimate or an acknowledgement depending on enquiry type. Estimates are examples only, not live quotes or stock checks.
- Contact form validates the sender's details and message, compiles the fields into a `mailto:` link and opens the visitor's default email application. The user must review and send the email.
- Contact page uses Leaflet with OpenStreetMap tiles and two approximate, illustrative Pretoria area markers. They are not exact business addresses.
- FAQ accordion behaviour is supported by reusable `.accordion-trigger` elements if added to a page.

## 3. Forms and processing limitations
Both forms use client-side HTML/JavaScript validation. The enquiry form calculates an example estimate in the browser and does not store or transmit personal data. The contact form prepares an email in the visitor's email client. A static HTML site cannot securely process or store form submissions by itself; a production deployment should connect a trusted form backend (for example Netlify Forms or a server-side endpoint) and replace the demo email address. The `.example` email recipient is deliberately non-deliverable and must be replaced with an authorised real recipient before live use.

## 4. SEO and performance
- Each HTML page has a unique title and meta description, responsive viewport, robots directive and social sharing metadata.
- Semantic page structure, descriptive headings, internal navigation, meaningful image alt text and descriptive page filenames are used.
- `robots.txt` and `sitemap.xml` are included. Replace `YOUR-SITE-NAME` in both files with the final Netlify subdomain before publishing.
- Images are compact SVG illustrations; non-critical product images use lazy loading. JavaScript is loaded with `defer`. CSS and JS are local files; Leaflet is loaded from its official CDN with Subresource Integrity attributes.
- Use HTTPS on the hosting platform. Do not place API keys, passwords or private credentials in client-side files.

## 5. Local testing
1. Extract the project folder and open `index.html` in a modern browser, or run a local static server from the project directory (for example `python -m http.server 8000`).
2. Open `http://localhost:8000` and test all navigation links.
3. On `products.html`, test keyword search, category filtering, all sorting options and the no-results message.
4. On `index.html`, open each gallery image, close with the close button, backdrop and Escape key.
5. On `enquiry.html`, submit empty/invalid fields, then a valid product enquiry and a volunteer/sponsor enquiry. Check the illustrative estimate and reset behaviour.
6. On `contact.html`, test invalid fields and a valid message. Confirm that the email app opens with all fields populated. The recipient is a placeholder.
7. Confirm the Leaflet map loads with an internet connection.
8. Test responsive layouts at approximately 390px, 768px and 1440px, and keyboard navigation/focus visibility.

## 6. Deployment (Netlify)
1. Push this project folder to a GitHub repository.
2. In Netlify, choose **Add new site → Import an existing project**, connect GitHub and select the repository.
3. For this plain HTML/CSS/JS project, leave the build command blank and set the publish directory to the repository root (`.`).
4. Deploy, open the generated HTTPS URL and test every page and form.
5. Replace `YOUR-SITE-NAME` in `robots.txt` and `sitemap.xml` with the actual Netlify subdomain, commit and push the changes, then redeploy.
6. Add the final live URL and repository URL to your LMS submission. Deployment and GitHub push require your own account sign-in and cannot be completed from this offline project package.

## 7. Git commands
```bash
git add .
git commit -m "Complete Part 3 JavaScript functionality and SEO"
git push origin main
```

## 8. Changelog and references
See `changelog.md` and `references.md`. No Part 2 lecturer feedback was supplied; therefore, no feedback has been invented. Part 3 improvements are recorded as independent enhancements and corrections identified during review.

## 9. Student project note
Golden Crust Bakery, its proposed service areas, prices and contact details are fictional project content. Do not present them as verified real-world business information.
