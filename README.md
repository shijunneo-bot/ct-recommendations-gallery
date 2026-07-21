# CleverTap Field Guide 07 — Recommendations & Catalogs

A single self-contained web gallery of 120 personalization plays across 15 verticals,
each one dressed as its own brand. Built for CSM client calls: fast to open, quick to
scan, and grounded in what CleverTap can actually ship today.

**Live once deployed:** `https://shijunneo-bot.github.io/ct-recommendations-gallery/`

---

## What is inside

- **The Cascade cover.** A 3D train of landscape brand mockups drifting toward you.
  Tap any card to drop straight into that vertical's shelf, or open the whole library.
- **120 plays, 15 verticals, 8 each.** Every card carries the renders, the trigger, the
  catalog CSV shape, the recipe, the APIs, and the outcome.
- **Per-vertical brand identity.** Each vertical owns a colour that flows through the
  mockups, the modal, and the Template Studio.
- **Template Studio, Docs, and Which Tool When.** Channel templates with copy-paste
  recipes, catalog CSV and upload docs, and a clean split of Recs vs Catalog vs Linked
  Content vs KVP.

## World-class pass (this build)

- **Day and night mode.** A visible toggle (top-right, bottom-right on mobile). It
  follows the visitor's system preference by default and remembers their choice. Both
  themes were contrast-audited: primary text clears WCAG AA comfortably in each (light
  around 18:1, dark around 15:1), and the amber accent was deepened in light mode so it
  stays legible on paper. The intro cover stays cinematic dark on purpose.
- **CleverTap favicon.** The tab icon is now the CleverTap "C on blue", matching the
  corporate favicon rather than a per-guide mark, so the whole family reads as one suite.
  The exact brand blue is easy to swap in the head if the brand book differs.
- **Search and AI discoverability.** Full canonical, description, keywords, Open Graph,
  and Twitter card metadata, plus JSON-LD structured data (WebSite, TechArticle,
  BreadcrumbList). A social share image (og.png) ships alongside.
- **Deep-linkable plays.** Every play has its own URL (.../#c/<ID>), so a single card
  can be shared, bookmarked, or cited. Opening a card updates the address bar; closing
  it clears it.
- **Crawlable play index.** A text index of all 120 plays, grouped by vertical, sits
  near the foot of the page with a direct link to each one.
- **The full family strip.** All ten guides are linked, with 07 marked as the current page.

## How it is built

- One HTML file. All CSS and JS are inline. No build step, no framework.
- The only external request is Google Fonts. Everything else, including the mockup tiles,
  the favicon, and the theme logic, is embedded.
- Works on desktop and mobile. Motion respects prefers-reduced-motion.

## Deploy on GitHub Pages

1. Create a new public repo named ct-recommendations-gallery on the shijunneo-bot account.
2. Add index.html, README.md, and og.png to the repo root on the main branch.
3. In Settings > Pages, set the source to Deploy from a branch, branch main,
   folder / (root), and save.
4. Give it a minute, then open
   https://shijunneo-bot.github.io/ct-recommendations-gallery/

Command-line version, from inside this folder:

    git init
    git add index.html README.md og.png
    git commit -m "FG07 Recommendations & Catalogs gallery"
    git branch -M main
    git remote add origin https://github.com/shijunneo-bot/ct-recommendations-gallery.git
    git push -u origin main

Then enable Pages in Settings as above.

## The Field Guide family

- 01 AMP Email — amp-email-gallery
- 02 Rich Push — rich-push-gallery
- 03 SMS — ct-sms-field-guide
- 04 WhatsApp — whatsapp-addon-gallery
- 05 Custom HTML In-App — ct-template-gallery
- 06 Linked Content — ct-linked-content-gallery
- 07 Recommendations & Catalogs — this repo
- 08 Geofencing — ct-geofencing-gallery
- 09 Reminders — ct-reminders-gallery
- 10 Promos — ct-promos-gallery

## One thing to verify before a client call

The Catalog API completion-endpoint name in the Docs tab was not confirmed against the
live reference. Check docs.clevertap.com before quoting the exact endpoint to a customer.
