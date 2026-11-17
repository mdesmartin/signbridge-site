# signbridge-site

Public page for the SignBridge iOS app, served with GitHub Pages from `main` at https://signbridge-app.com (custom domain since 2026-11-17, `CNAME` file; domain at OVH, DNS zone: four A and four AAAA records to GitHub Pages, `www` CNAME to `mdesmartin.github.io`, OVH MX for mail). The old https://mdesmartin.github.io/signbridge-site/ addresses redirect to it.

- `index.html`, `privacy.html`: French
- `en/index.html`, `en/privacy.html`: English
- `style.css`: shared styles, dark like the App Store screens (near black `#17130F`, cream `#F6EEE2`, grey `#8F8476`, one orange `#F28224`, SF). Bump `?v=` in the pages when it changes, Safari caches it.
- `img/`: logo, favicon, the horizon background (from the App Store header) the official App Store badges (Apple kit, black lockup) and one iPhone screenshot, Pompier (Adonis's image consent covers the website)

The wording comes from the 1.1 App Store page (`signbridge-brain/marketing/app-store.md`) and the final App Store screens; reuse it rather than writing new text.

The page never gives a number of signs or a list of them: the vocabulary grows with each version.

App Store Connect URLs (keep these paths):

- Marketing: https://signbridge-app.com/
- Support: https://signbridge-app.com/#support
- Privacy policy: https://signbridge-app.com/privacy.html

Both languages have the same height for every chapter, at every screen width: each text block also holds the other language's text, invisible (`.jumeau` / `.fantome`), so it takes the room of the longer of the two. Edit the French and English texts together.

Search and sharing (2026-11-17, SB-103):

- Each page has a canonical URL and `hreflang` links (fr, en, x-default = English); `sitemap.xml` lists the four pages with their alternates. Submit it in Google Search Console (URL-prefix properties for the old address and `https://signbridge-app.com/`, verified with the meta tag in `index.html`). A project site cannot have its own `robots.txt` (it would sit at the domain root); not needed.
- Titles and descriptions aim at real searches (« langue des signes », LSF, iPhone, hors ligne) and reuse the App Store wording; never « traduire ».
- Open Graph and Twitter tags use `img/og-fr.jpg` / `img/og-en.jpg` (1200 × 630, made from the App Store header with a dark band on top).
- `apple-itunes-app` shows Safari's Smart App Banner on iPhone.
- JSON-LD `MobileApplication` describes the app for search engines; update it if the price or the languages change.
