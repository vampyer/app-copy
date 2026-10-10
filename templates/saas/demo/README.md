# Launch — SaaS product landing page

A responsive, accessible SaaS product landing page built with plain HTML and CSS. No build step, no frameworks, no dependencies — open `index.html` in a browser and it works.

- **Files:** `index.html`, `style.css`, `script.js` (mobile menu toggle only)
- **Fonts:** Plus Jakarta Sans (loaded from Google Fonts; falls back to system fonts offline)
- **Sections:** Header with mobile menu, hero with CSS-built product mockup, logo strip, 6-feature grid, testimonial, 3-tier pricing, FAQ accordion (native `<details>`, no JS), call-to-action banner, footer.

## How to edit

1. Open the folder in any code editor (VS Code is free) and open `index.html` in your browser side by side.
2. **Text:** edit the words directly in `index.html`. Every section starts with a comment like `<!-- ========== PRICING ========== -->` so it's easy to find.
3. **Colors & fonts:** open `style.css`. The main colors, fonts, spacing and corner radius are CSS variables in the `:root { … }` block at the very top — change them there and the whole page updates. (A few decorative illustrations use fixed colors inside their SVG code; edit those directly if needed.)
4. **Changing fonts:** pick fonts on [fonts.google.com](https://fonts.google.com), replace the `<link href="https://fonts.googleapis.com/…">` line in `index.html` with the new one, then update the `--font-…` variables in `style.css`.
5. **Page title & description:** update `<title>` and `<meta name="description">` in the `<head>` — these are what Google shows in search results.
6. **Images:** all artwork is inline SVG or CSS, so there are no image files to manage. You can swap any of it for your own photos (see tips below). Always write a short, descriptive `alt` text for real images.

### Template-specific tips

- **Brand colors:** change `--primary` (buttons, highlights) and `--accent` (eyebrows, gradient end). The hero gradient text and CTA banner pick these up.
- **Product screenshot:** the hero mockup is pure HTML/CSS. To use a real screenshot, replace the whole `<div class="mockup">…</div>` with `<img src="screenshot.png" alt="Describe your screenshot" class="mockup">`.
- **Customer logos:** each logo in the strip is a small inline SVG. Swap in your customers' SVG logos (keep `aria-label` with the company name).
- **Pricing:** edit the three `<article class="plan">` blocks. The middle one has `plan-featured` — move that class to highlight a different plan.
- **FAQ:** copy a `<details>…</details>` block to add a question. Add the `open` attribute to have one expanded by default.

## How to deploy for free

**Option A — Netlify Drop (easiest, ~1 minute)**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag this whole folder onto the page.
3. You get a live URL instantly. Create a free account to keep it and connect your own domain.

**Option B — GitHub Pages**
1. Create a free account at [github.com](https://github.com) and make a new public repository.
2. Click **Add file → Upload files** and upload `index.html`, `style.css` and any other files in this folder (not the folder itself).
3. Go to **Settings → Pages**, set **Source** to “Deploy from a branch”, choose `main` and `/ (root)`, then **Save**.
4. After a minute your site is live at `https://<your-username>.github.io/<repo-name>/`.

Other free options that work the same way: Cloudflare Pages, Vercel, Render static sites.

## Accessibility notes

Semantic landmarks (`header`, `nav`, `main`, `footer`), a skip-to-content link, visible keyboard focus styles, labelled form fields, decorative graphics hidden from screen readers, and `prefers-reduced-motion` support are built in. Keep them when you edit, and check that any new colors keep text readable (aim for 4.5:1 contrast — [webaim.org/resources/contrastchecker](https://webaim.org/resources/contrastchecker/)).

## License

Use for unlimited personal and client projects. Do not resell or redistribute the template files themselves.
