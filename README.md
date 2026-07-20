# CleverTap Field Guide 07 — Recommendations & Catalogs

A single self-contained web gallery of 120 personalization plays across 15 verticals,
each one dressed as its own brand. Built for CSM client calls: fast to open, quick to
scan, and grounded in what CleverTap can actually ship today.

**Live once deployed:** `https://shijunneo-bot.github.io/ct-recommendations-gallery/`

---

## What is inside

- **The Cascade cover.** A 3D train of landscape brand mockups drifting toward you,
  wordmark bottom-left. Tap any card to drop straight into that vertical's shelf, or
  open the whole library.
- **120 plays, 15 verticals, 8 each.** Every card carries the renders, the trigger, the
  catalog CSV shape, the recipe, the APIs, and the outcome. No filler.
- **Per-vertical brand identity.** Each vertical owns a colour that flows through the
  mockups, the modal, and the Template Studio. StyleCo, AsiaBank, MakanGo, FlyAsia and
  the rest.
- **Template Studio.** 10 channel templates (email digest, standard and rich push,
  countdown timer, in-app, app inbox, web push, SMS, WhatsApp carousel), each with a
  copyable recipe and a five-step "run it on CleverTap" setup.
- **Docs tab.** Catalog CSV prep, the pre-signed URL upload flow, event mapping, the
  publish window, the PBS rule, and Catalog STP Liquid.
- **Which Tool When.** A short breakdown of Recs vs Catalog vs Linked Content vs KVP so
  the four never get confused on a call.

## The look

Editorial noir in amber and gold. A coarse pixel grain over a warm gradient, a cursor
glow that brightens over anything interactive, and a light spike that fires at the
pointer on click. All motion respects `prefers-reduced-motion`.

## How it is built

- One HTML file. All CSS and JS are inline. No build step, no framework.
- The only external request is Google Fonts (Space Grotesk, Inter, IBM Plex Mono).
  Everything else, including the mockup tiles and the favicon, is embedded.
- Works on desktop and mobile. The cascade becomes a snap-scroll row on small screens.

## Deploy on GitHub Pages

1. Create a new public repo named `ct-recommendations-gallery` on the `shijunneo-bot`
   account.
2. Add `index.html` and this `README.md` to the repo root on the `main` branch.
3. In **Settings > Pages**, set the source to **Deploy from a branch**, branch `main`,
   folder `/ (root)`, and save.
4. Give it a minute, then open
   `https://shijunneo-bot.github.io/ct-recommendations-gallery/`.

Command-line version, from inside this folder:

```bash
git init
git add index.html README.md
git commit -m "FG07 Recommendations & Catalogs gallery"
git branch -M main
git remote add origin https://github.com/shijunneo-bot/ct-recommendations-gallery.git
git push -u origin main
```

Then enable Pages in Settings as above.

## After it is live

Add the FG07 link to the family strip on the five older galleries so the suite stays
connected:

- 01 AMP Email — `amp-email-gallery`
- 02 Rich Push — `rich-push-gallery`
- 03 SMS — `ct-sms-field-guide`
- 04 WhatsApp — `whatsapp-addon-gallery`
- 05 Custom HTML In-App — `ct-template-gallery`
- 06 Linked Content — `ct-linked-content-gallery`
- 07 Recommendations & Catalogs — this repo

## A note on the favicon

The tab icon is an amber spark in the guide's own identity, not the official CleverTap
corporate mark. To use the corporate favicon instead, drop the asset in and swap the
`<link rel="icon">` data URI in the `<head>`.

## One thing to verify before a client call

The Catalog API completion-endpoint name in the Docs tab was not confirmed against the
live reference. Check `docs.clevertap.com` before quoting the exact endpoint to a
customer.
