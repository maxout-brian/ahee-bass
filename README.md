# AHEE — Website Concept Prototype

A clickable, multi-page concept for the AHEE site, built as static HTML for client walkthrough. All pages share one design system and link to each other, so you can navigate the whole thing like a real site.

## Pages
| File | Page | Notes |
|------|------|-------|
| `index.html` | Home | Hero carousel, Shop Merch / Shop Music teasers, tour list, newsletter |
| `music.html` | Shop Music collection | Software + Sound filters, live product grid |
| `merch.html` | Shop Merch collection | 5 products, inline size/variant selection, add-to-cart |
| `tour.html` | Tour | Poster hero + date list with on-sale / sold-out / coming-soon states |
| `product.html` | Product detail | Edition variant, details, metadata-driven recommendations |

The top nav works on every page; the homepage "view all" links and the music-collection cards deep-link through to the right pages.

## What's real vs. placeholder
- **Real:** layout, design system, filtering/variant/cart interactions, page-to-page navigation.
- **Placeholder — swap before any public use:** all imagery (hero, product tiles, tour poster are CSS stand-ins), tour dates/venues, ticket URLs (`href="#"`), several invented product names, and the shipping/returns copy.
- No backend: newsletter and cart are in-memory only (reset on refresh). On the real build these connect to Shopify / Klaviyo.

---

## Put it on GitHub + publish for the walkthrough

You'll do these steps (they need your GitHub login — that part can't be delegated). A GitHub **repo** alone isn't clickable for a client; **GitHub Pages** turns it into a live URL, which is what you want for the walkthrough.

### Option A — GitHub Desktop (no command line)
1. Create a new repo on github.com (e.g. `ahee-site-concept`). Keep it **private** if you don't want it public — note Pages on a private repo needs a paid plan; if it's a throwaway concept, a public repo is simplest.
2. Open GitHub Desktop → **File → Clone repository** → pick the new repo.
3. Copy all files from this `ahee_site` folder into the cloned folder.
4. In GitHub Desktop: write a summary ("Initial concept"), **Commit to main**, then **Push origin**.
5. On github.com → repo → **Settings → Pages** → under "Build and deployment," Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)** → Save.
6. Wait ~1 minute. Pages shows your live URL: `https://<your-username>.github.io/ahee-site-concept/`. That's the link you send / open in the meeting.

### Option B — Command line
```bash
cd ahee_site
git init
git add .
git commit -m "Initial AHEE site concept"
git branch -M main
git remote add origin https://github.com/<your-username>/ahee-site-concept.git
git push -u origin main
```
Then do step 5–6 above (Settings → Pages) to get the live URL.

### Walkthrough tip
Open the live Pages URL, not the raw files — links, fonts (Google Fonts), and layout all behave exactly as they will for the client. Start on `index.html` and click through the nav.
