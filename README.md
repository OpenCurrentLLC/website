# OpenCurrent — Static Site (Netlify)

Brochure site for OpenCurrent. Plain HTML and CSS, no build step.

Pages:
- `/` — Home
- `/about.html` — Team
- `/contact.html` — Contact (Netlify form)
- `/thanks.html` — Post-submit (noindex)

## Editing
- Each page carries its own header and footer markup; keep them in sync when changing nav or footer links.
- Styles live in `assets/css/styles.css`. Palette and type are set as CSS variables at the top.
- Fonts (Source Serif 4, Source Sans 3) load from Google Fonts; the CSS falls back to Georgia and system sans if they fail.
- Logo mark: `assets/img/logo.svg` (header, footer) and `assets/img/favicon.svg`. Share image: `assets/img/og-image.jpg` (1200×630).
- The site domain is assumed to be `https://opencurrent.us` in canonical/OG tags, `robots.txt`, and `sitemap.xml`. Search and replace if that changes.

## Images
- Hero and banner photos are Unsplash (Karsten Winegeart, Jessica Furtney), credited in the footer.
- Originals live in `assets/img/possibilities/` (git-ignored). Optimized copies are `hero-braided*`, `banner-channels*`, and `gorge*` in both `.jpg` and `.webp`.
- To regenerate an optimized image: `convert in.jpg -strip -resize 2200x -quality 72 out.jpg && cwebp -q 70 out.jpg -o out.webp`.
- Team headshots are cropped square by CSS; any reasonably tight portrait works.

## Placeholders left to fill
- Footer "Connect" column: email, LinkedIn, location (commented out in each page).
- Team cards: per-person links (commented out in `about.html`).
- Home page: proof sections for track-record numbers and partner logos (commented skeleton in `index.html`).

## Deploy
Push to GitHub and connect the repo in Netlify. Enable form notifications in Netlify (Forms → contact → Notifications).
