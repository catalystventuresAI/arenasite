# Arena Partners — Website

Static site for https://arenapartners.com with three pages:
- `index.html`: homepage
- `how-it-works.html`: How it works
- `contact.html`: contact page

`support.js` is the small runtime that `index.html` and `contact.html` need, so keep it in the same folder. Fonts (IBM Plex Sans, Newsreader) load from Google Fonts.

## Updating the live site
Replace the files in the repo root with these, commit, and push. Vercel redeploys automatically.

## First-time deploy on Vercel
1. Push this folder to a GitHub repo (index.html at the repo root).
2. In Vercel: New Project → import the repo.
3. Framework preset: **Other**. Build command: none. Output directory: `.` (root).
4. Deploy.

## Local preview
Run `npx serve .` and open the printed URL.

## SEO / GEO
- Every page has a title, meta description, canonical URL, Open Graph and Twitter tags, a favicon, and schema.org JSON-LD (Organization with team members, WebSite, Service, ContactPage, and breadcrumbs).
- `robots.txt` allows all search crawlers and AI crawlers, and points to `sitemap.xml`.
- `llms.txt` is a plain-language summary of the site for AI assistants.
- After launch, submit `https://arenapartners.com/sitemap.xml` in Google Search Console and Bing Webmaster Tools.
- If you add pages, add them to `sitemap.xml` and `llms.txt`.

## Notes
- LeadBoxer tracking is installed in the `<head>` of every page, right after Google Analytics.
- Any URL that doesn't exist goes to `404.html`, which sends visitors to the home page straight away. Vercel uses `404.html` automatically, so no configuration is needed. The page still returns a 404 status, so search engines won't index broken URLs.
- Google Analytics (G-WCY68JY0X6) is installed in the `<head>` of every page.
- Team headshots live in `images/`. Upload that folder too.
- "How we work" in every header and footer links to `how-it-works.html`.
- **Contact form (Web3Forms):** the access key is already set in `contact.html`. Submissions are emailed to the address registered with that key. To change where they go, create a new key at https://web3forms.com and replace the key in `contact.html`.
