# EROOE — Corporate Website

Static, fast, RTL-first site (Persian) built on the "Obsidian Kinetic" design system. No runtime dependencies.

## Run
    python3 -m http.server 8000   # or any static server, then open http://localhost:8000
(Serve over http — the strict CSP in each page's <meta> does not work from file://.)

## Edit
- Shared header/footer/components and page copy: `build.mjs` → run `node build.mjs` to regenerate the 5 pages.
- Styles: `assets/css/styles.css` (design tokens in `:root`). Behaviour: `assets/js/main.js`.
- Real domain for canonical/sitemap: `SITE_URL=https://yourdomain.com node build.mjs`.
- Contact form: set `data-endpoint` on `#contact-form` (in build.mjs) to your form backend URL. Until then the form validates but tells the visitor it is not connected (it never fakes success).

## Placeholders
Anything not provided (email, phone, address, map, social links, extra team members, dates, user stats) is marked with a dashed `.ph` tag. Search for `class="ph"` in build.mjs.
