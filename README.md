# Velmora Estates

> "Exceptional Properties. Extraordinary Living."

Velmora Estates is a luxury real estate website **demo**, customized by **Muhammad Azhan** from an existing template. It is built with plain HTML5, CSS3 and JavaScript (ES6+), with no frameworks, no build step and no npm dependencies.

**Everything shown is fictional sample content:** the 24 properties, the six advisors, the testimonials, the statistics and the phone numbers and emails inside the sample data. Velmora Estates is not a real agency. The inquiry, valuation, viewing and newsletter forms are demos: they validate input and show loading states, but **nothing is sent or stored**.

- Live demo: not deployed yet
- Developer portfolio: https://muhammadazhan.dpdns.org

## Developer

| | |
|---|---|
| Name | Muhammad Azhan, Web Developer \| Full Stack Developer |
| GitHub | https://github.com/Azhan787 |
| LinkedIn | https://www.linkedin.com/in/muhammad-azhan-54724537a |
| Email | itxazhan32@gmail.com |
| WhatsApp | +92 370 136 6877 (https://wa.me/923701366877) |

## Features (tested in a real browser unless marked otherwise)

- **Search and filters:** keyword search (150 ms debounce), status, location, type, price, bedrooms, bathrooms, minimum area and amenity filters, "clear all filters". Keyword search and clear were tested; the remaining individual filters were not tested one by one.
- **Sorting:** featured, price low to high, price high to low, popularity, newest. Price ascending was tested.
- **Favorites:** save and remove residences, header and drawer counters, a saved-properties view (`#favorites`), stored in `localStorage` under `velmora_favorites`. Saving, the counter, the `#favorites` view and persistence after reload were tested.
- **Property details:** modal with gallery thumbnails, specifications, amenities and advisor card. Opening, focus handling and keyboard behavior were tested.
- **Fullscreen lightbox:** Left/Right arrows change the photo and Escape closes it. Tested.
- **Schedule a viewing:** modal pre-filled with the property name, with inline validation. Validation was tested. A fully valid submission was not tested.
- **Mortgage calculator:** four sliders update the monthly payment instantly. Tested.
- **Forms:** contact, valuation, viewing and newsletter forms with inline validation and button-level loading states. The contact form (empty and valid) and the newsletter form were tested. The valuation and viewing forms' success paths were not.
- **Routing:** `#buy` and `#favorites` were tested. `#rent` uses the same code path but was not tested.
- **Share:** Web Share API with a clipboard fallback. Implemented, not tested.
- **Responsive layout:** tested for horizontal overflow at 17 widths from 320px to 1920px.
- **Accessibility:** skip link, `<main>` landmark, dialog roles, focus moved into dialogs and returned on close, Tab kept inside open dialogs, closed dialogs removed from the tab order, visible keyboard focus, `prefers-reduced-motion` support.

## What changed from the original template

- Rebranded from "Aurevia Estates" to **Velmora Estates** (title, header, footer, metadata, Open Graph and Twitter tags, favicon, data variable `VELMORA_DATA`, storage key).
- Replaced the fictional agency's contact details, social links and legal line with the developer's real contact details, and removed the fictional "LLC" and "Equal Housing" wording.
- Marked the site clearly as a demo (hero note, contact section, footer, form messages). Form success messages previously claimed an inquiry had been "routed to our Senior Partners"; they now say nothing was sent.
- Sample data: advisor phone numbers replaced with reserved or obviously fake numbers, advisor emails moved to the reserved `velmora.example` domain, a testimonial attributed to a royal title replaced with a neutral sample client, and mentions of real publications as press placements removed.
- Responsive fixes (details below), keyboard and screen-reader fixes, a 44px minimum touch size on touch layouts, and a wider hamburger-menu range (the full desktop nav only fits from 1280px).
- The original design system (fonts, colors, spacing, components) is unchanged.

### Root causes fixed

- Grid columns used `1fr` tracks, which can grow to fit long content. They are now `minmax(0, 1fr)`, and grid children can shrink (`min-width: 0`).
- `body { overflow-x: hidden }` was hiding overflow instead of fixing it. It was removed after the causes were fixed.
- Fixed `min-width` values (search box, toasts) larger than a 320px screen now use `min()`.
- The hero tabs, footer newsletter field and contact cards forced their parents wider.
- The 9-link desktop nav overflowed the header between 1025px and about 1440px.

## Technologies

HTML5, CSS3 (custom properties, Grid, Flexbox) and vanilla JavaScript.
External resources loaded at runtime: Google Fonts (Cinzel, Playfair Display, Plus Jakarta Sans), Font Awesome 6.5.1 from cdnjs, and property, advisor and avatar photos hot-linked from Unsplash.

## Run it

No build step or server is needed. Open `index.html` in a modern browser, or serve the folder with any static host (GitHub Pages, Netlify, Vercel).

## Files

```
index.html     page structure and modals
styles.css     design system, layout and responsive rules
data.js        sample properties, advisors, services, statistics and testimonials
app.js         filters, modals, favorites, calculator, forms and routing
favicon.svg    site icon
README.md      this file
```

## Known limitations

- Photos are hot-linked from Unsplash, so they need an internet connection. Their licensing and availability were not checked, and the people shown as advisors and clients are stock photos.
- The forms have no backend. To receive real messages, connect a form service or your own endpoint in the submit handlers in `app.js`.
- `og:image` and `og:url` are not set, because there is no deployed URL or share image yet.
- Tested in Chromium only. Safari, Firefox and real phones were not tested.
- In the test environment Google Fonts and Font Awesome could not load, so similar local fonts and placeholder icons stood in for them. Check the final typography and icons in a normal browser.

## Attribution and license

This project was customized from an existing template. The supplied files contained no license file and no source URL, so the original author and license are **unknown**. The original README carried this notice, which is preserved here:

> &copy; 2026 Aurevia Estates International Realty LLC. All Rights Reserved.

Check the original source and its license before publishing or redistributing this project. No license is claimed for the original code or content. Muhammad Azhan's modifications are described in the section above.
# Velmora-Estates
