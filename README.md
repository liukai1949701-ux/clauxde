# Plainpage storefront

This repository hosts the sales page for **Plainpage** — a pack of four landing page
templates (SaaS, Waitlist, Portfolio, Digital product) in plain HTML and CSS, sold
as a one-time $19 download.

> **The paid product is not in this repository.** This repo is public, so anything
> committed here can be downloaded for free. The template pack (`plainpage-v1.0.zip`)
> is uploaded to the store only. Never commit it here.

```
docs/                  The storefront, served by GitHub Pages
  index.html           Sales page (built with the Digital product template)
  style.css
  config.js            ← your checkout link goes here
  img/                 Template screenshots + social share image (og.jpg)
marketing/
  cover-1280x720.jpg   Cover image for your store listing
  thumbnail-600x600.jpg Thumbnail for your store listing
```

---

## Launch checklist

### 1. Put the storefront online (free, ~2 minutes)

1. Merge this branch into `main`.
2. On GitHub: **Settings → Pages → Build and deployment**.
   Source: **Deploy from a branch** · Branch: **`main`** · Folder: **`/docs`** → **Save**.
3. After a minute the page is live at
   **https://liukai1949701-ux.github.io/clauxde/**

Until you add a checkout link, every buy button shows "Coming soon", so it's safe to
publish right away.

*Optional:* rename the repository to `plainpage` (Settings → General) for a nicer URL,
then update the two `https://liukai1949701-ux.github.io/clauxde/` addresses in the
`<head>` of `docs/index.html`.

### 2. Create the product in a store

Pick one. All three handle payment, delivery of the download and receipts.
**Check that the platform can pay out to your country and bank before you choose.**

| Platform        | Fees (check current pricing)         | Notes |
| --------------- | ------------------------------------ | ----- |
| Gumroad         | Percentage per sale, no monthly fee  | Simplest to set up; handles sales tax/VAT as merchant of record |
| Lemon Squeezy   | Percentage + small fixed fee per sale | Merchant of record (handles VAT/sales tax) |
| Payhip          | Free plan with a percentage fee      | Also supports memberships and coupons |

When creating the product:

- **File:** upload `plainpage-v1.0.zip`
- **Price:** $19 (the storefront shows $19 — change both together if you change it)
- **Cover / thumbnail:** `marketing/cover-1280x720.jpg`, `marketing/thumbnail-600x600.jpg`
- **Refunds:** the storefront promises a **14-day refund**. Set the same policy in the
  store, or edit the "14-day refund" box in `docs/index.html`.
- **Description:** use the copy below.

### 3. Connect the buy buttons

Open `docs/config.js`, paste your product's checkout link between the quotes, commit
and push:

```js
window.CHECKOUT_URL = "https://yourname.gumroad.com/l/plainpage";
```

Every buy button on the page now points to your checkout. Only `https://` links are
accepted.

### 4. Make a test purchase

Most platforms offer a test mode or a 100%-off discount code. Buy your own product
once to confirm the download and receipt email work.

### 5. Tell people about it

A store page with no visitors makes no sales. Distribution is most of the work:

- **Give one template away free.** Publish one template (for example Waitlist) as a
  free, open-source repo with a link to the full pack. Free templates get shared and
  found on GitHub and Google; the paid pack is the upgrade.
- **Show your work where builders hang out:** Reddit (r/SideProject, r/webdev's
  Showoff Saturday, r/web_design), Indie Hackers, Hacker News ("Show HN"),
  Product Hunt, X/Twitter, Mastodon, Bluesky. Read each community's self-promotion
  rules first.
- **Write one useful article**, e.g. "A landing page in under 30 KB with no JavaScript"
  on dev.to, Hashnode or Medium, linking to the storefront.
- **List on marketplaces with built-in traffic:** Gumroad Discover, and template
  directories that accept HTML templates.
- **Ask your first buyers for feedback** and, with permission, a short quote you can
  add to the page. (Only ever use real quotes.)

---

## Store listing copy

**Title**
Plainpage — 4 landing page templates in plain HTML & CSS

**Short description**
Four hand-crafted landing pages for SaaS products, app waitlists, freelance
portfolios and digital products. No frameworks, no build step, no JavaScript.

**Description**

Launch a beautiful landing page this afternoon.

Plainpage is four complete, hand-crafted landing page templates written in plain
HTML and CSS. Open a file, change the words, and publish — no frameworks, no build
tools, no JavaScript to break.

What's included:

- **SaaS** — hero with product mock, features, how it works, three-tier pricing, FAQ and call to action
- **Waitlist** — email signup (works with Formspree, Mailchimp, Kit and others), highlights, roadmap and FAQ
- **Portfolio** — editorial layout with selected work, services, about, testimonial and contact
- **Digital product** — sales page with buy box, contents, preview gallery, author, offers, guarantee and FAQ

Every template:

- Light and dark mode, following the visitor's system setting
- Responsive from small phones to wide screens
- Accessible: semantic HTML, skip links, visible keyboard focus, AA contrast
- Under 30 KB per page, with no trackers, web fonts or CDNs
- Re-theme by changing a few CSS variables
- SEO and social-sharing meta tags

Also included: a step-by-step guide to customising, connecting forms and buy
buttons, and publishing free on GitHub Pages, Netlify or Cloudflare Pages.

Licence: use on unlimited personal and client websites. Reselling or redistributing
the templates themselves is not allowed.

**Tags**
landing page, html template, css template, website template, saas template,
portfolio template, waitlist page, static site, no javascript

---

## Updating the storefront

The page is plain HTML: edit `docs/index.html`, commit and push to `main`, and GitHub
Pages redeploys within a minute or two.
