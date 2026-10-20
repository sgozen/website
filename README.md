# suleymangozen.com

One-page academic site. Everything lives in `index.html`; no build step, no dependencies.

## Test it (no domain involved)

1. Create a **public** repo on GitHub and upload every file in this folder.
2. `Settings > Pages > Build and deployment`: source `Deploy from a branch`, branch `main`, folder `/ (root)`.
3. After a minute the site is live at `https://<username>.github.io/<repo>/`.
   `robots.txt` blocks search engines while you are testing, so this address will not show up in Google.

## Go live on the domain

1. Rename `CNAME.txt` to `CNAME` (no extension).
2. `Settings > Pages > Custom domain`: `www.suleymangozen.com`, then tick `Enforce HTTPS`.
3. At your DNS provider, point `www` to `<username>.github.io` with a CNAME record, and remove the
   Google Sites domain mapping.
4. Done: `robots.txt` now allows indexing.
5. Only now unpublish the Google Sites page.
6. In Google Search Console, verify the domain and submit `sitemap.xml`.

## Editing

- Papers, talks, teaching: plain HTML lists in `index.html`, each entry is one `<li>`.
- A paper entry: title in `<h3>`, then the `Draft` link, the status label, the co-authors, then the
  `<details class="abs">` block holding the abstract.
- Colours and fonts: the `:root` block at the top of the `<style>` section.
- `photo.jpg` and `workshop.jpg` are referenced by file name; replace them with same-named files to swap images.

The folders `research/`, `teaching/`, `cv/` and `intangible-capital-workshop/` only redirect the old
Google Sites addresses to the matching section of the new page.
