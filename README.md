# Thermic Mobile Sauna — Website

Single-page site for Thermic Mobile Sauna in Ann Arbor, MI. Static HTML, no build step required.

## Files

```
index.html              Home page
gallery.html            Photo gallery page
thermic-logo.png        Logo (used in nav, OG preview, apple-touch-icon)
photo-driveway.jpg      Gallery: parked trailer, driveway
photo-firing-up.jpg     Gallery: smoke from the chimney
photo-interior.jpg      Gallery: back doors open, cedar interior
photo-dusk.jpg          Gallery: glowing flame at dusk
photo-gathering.jpg     Gallery: night, group around fire
favicon.svg             Browser tab icon
robots.txt              Tells search engines they're welcome
sitemap.xml             Lists pages for Google
README.md               This file
```

## Deploy

### GitHub Pages (easiest, free)

1. Push this folder to a new GitHub repo.
2. In the repo → **Settings → Pages**.
3. Under **Source**, select `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
4. Wait ~1 minute. Your site is live at `https://<your-username>.github.io/<repo-name>/`.
5. To use a custom domain (e.g. `thermicsauna.com`): add a `CNAME` file with just the domain inside, then point your domain's DNS at GitHub Pages (instructions: https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site).

### Netlify / Vercel (also free, drag-and-drop)

1. Zip this folder (or push to GitHub).
2. Netlify: drag the folder onto https://app.netlify.com/drop. Done.
3. Vercel: `npx vercel` from this folder, or import the GitHub repo at https://vercel.com/new. Done.

## After deploy — swap the placeholder domain

Every reference to `thermicsauna.com` inside the files assumes that's the final domain. Find-and-replace it to whatever you actually use. The places to check:

- `index.html` — `<link rel="canonical">`, Open Graph tags (`og:url`, `og:image`), Twitter tags, JSON-LD (`url`, `@id`, `image`, `logo`)
- `robots.txt` — `Sitemap:` line
- `sitemap.xml` — `<loc>` tag

## SEO next steps (bigger lift than this HTML)

1. **Google Business Profile** at https://business.google.com — this is 10x more impactful for local search than any on-page SEO. Takes about 15 minutes. Lists you in the "map pack" at the top of local results.
2. **Submit the sitemap** in Google Search Console at https://search.google.com/search-console once the site is deployed.
3. **Collect reviews** on Google and tag them with keywords like "mobile sauna," "sauna rental," "cold plunge," "Ann Arbor."

## Contact routing

All CTAs link to Nick at `(734) 531-8005` via `tel:` and `sms:` links. To change the number, search the file for `7345318005` and `(734) 531-8005` — update both.
