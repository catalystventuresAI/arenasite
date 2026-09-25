# Arena Partners — Homepage

Static homepage. `index.html` is the page; `support.js` is the small runtime it needs (keep them side by side). Fonts (IBM Plex Sans, Newsreader) load from Google Fonts.

## Deploy on Vercel
1. Push this folder to a GitHub repo (index.html at the repo root).
2. In Vercel: New Project → import the repo.
3. Framework preset: **Other**. Build command: none. Output directory: `.` (root).
4. Deploy.

## Local preview
Run `npx serve .` and open the printed URL.

## Notes
- Anchor links (`#why`, `#how`, `#contact`) scroll within the page. "Blog" and "Letter to investors" point to `#blog` / `#letter` placeholders. Replace them with real URLs when those pages exist.
- "Contact us" is `mailto:hello@arenapartners.com`. Update it if needed.
