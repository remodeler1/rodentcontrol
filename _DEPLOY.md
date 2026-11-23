# Murvo Rodent Control — rodentcontrol.us — FINAL build (V6)

This is ONE ordinary static website: 13,910 HTML pages plus assets. Every
internal link is relative, so it runs on any static host with no build step
and no server-side code.

## What's inside

- `index.html` — homepage
- `about.html`, `contact.html`, `services.html`, `editorial-policy.html`,
  `privacy-policy.html`, `terms-of-service.html`, `sitemap.html`, `404.html`
- `services/<service>.html` — the 30 core service pages
- `<state>.html` — 49 state/DC hub pages, each listing every city served in
  that state (e.g. `texas.html`, `district-of-columbia.html`)
- `<state>/rodent-control-<city>.html` — 13,822 city pages
  (e.g. `illinois/rodent-control-chicago.html`)
- `assets/` — CSS, JS, fonts and images (all local; no placeholder or
  third-party image endpoints)
- `sitemap.xml` — exactly the 13,909 indexable pages (all pages except
  404.html, which is noindex by design)
- `robots.txt` — declares the sitemap; blocks AI/scraper bots and
  parameter/search URLs for other crawlers
- `.htaccess` — Apache/LiteSpeed only: forces HTTPS, redirects www to
  non-www in one hop, serves the custom 404, enables compression, caching
  and security headers. Other hosts ignore it safely.

## Upload to shared hosting (cPanel, Hostinger, Namecheap, GoDaddy…)

1. Unzip this package.
2. Upload everything inside it into your web root (usually `public_html`),
   preserving the folder structure.
3. Point the domain at the host and make sure an SSL certificate is active
   (the .htaccess rules force HTTPS and set HSTS once HTTPS is seen).
4. Visit https://rodentcontrol.us — done.

## Drag-and-drop hosts (Netlify, Cloudflare Pages, Vercel)

Drop the unzipped folder into the deploy area. Note: Cloudflare Pages caps a
deployment at ~20,000 files — this build has ~14,800 files, so it fits.
`.htaccess` is ignored on those hosts; add equivalent HTTPS + www redirect
rules in the host's dashboard if you need them there.

## After upload

- Canonicals, `sitemap.xml`, `robots.txt` and all schema already point to
  https://rodentcontrol.us — nothing to find-and-replace.
- Submit `https://rodentcontrol.us/sitemap.xml` in Google Search Console
  and Bing Webmaster Tools.
- Spot-check: homepage, one state hub (e.g. /texas.html), one city page,
  and a nonsense URL to confirm the custom 404 responds.

## One outstanding item: the contact form

The contact form's markup is complete, but in the original static files it
posts to a platform endpoint that is not part of this package. On a plain
static host the form will not deliver leads until that endpoint is wired
(e.g. to your form/CRM inbox). Phone CTAs — (888) 842-2618 — work on every
page regardless.
