# Michael Rabasca, CPA — personal website

Static site. One page, no build step, no dependencies.

    index.html                     The whole page
    styles.css                     All styling (brand tokens at the top, under :root)
    michael-rabasca-resume.pdf     Linked from the hero and the footer
    favicon.png                    Browser tab icon

## Before you publish — check these

1. **Resume PDF** — `michael-rabasca-resume.pdf` is your 2025 resume. Replace the
   file (same name) whenever you update it; no HTML change needed.
2. **Audit employer** — the 2018–2021 role reads "PUBLIC ACCOUNTING — NEW YORK".
   Search `index.html` for that string and put the firm name in if you want it public.
3. **Email and phone** — `Mrabasca03@gmail.com` and `(908) 752-3556` appear in the
   footer. Swap in a different address if you would rather not publish your personal one.
4. **LinkedIn** — not currently linked. To add it, copy one of the `.foot-details`
   blocks in the footer and point it at your profile URL.
5. **Copyright year** in the footer.

## Deploy to GitHub Pages

1. Create a new **public** repository — `michael-rabasca` or `mrabasca.github.io`.
   (If you name it `<username>.github.io`, the site lives at the root domain.)
2. Upload the contents of this folder to the repository root — drag the files onto
   the "uploading an existing file" screen. `index.html` must sit at the top level.
3. Repository → **Settings** → **Pages** → Source: "Deploy from a branch",
   Branch: `main`, folder: `/ (root)`. Save.
4. Give it a minute. The site is live at
   `https://<your-username>.github.io/michael-rabasca/`.

## Custom domain

1. Buy a domain (Cloudflare Registrar or Namecheap, ~$12–15/yr) —
   `michaelrabasca.com` or similar.
2. At the registrar's DNS settings, add:
   - four `A` records for `@` → `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - one `CNAME` record for `www` → `<your-username>.github.io`
3. GitHub → Settings → Pages → Custom domain: enter the domain, save, then tick
   **Enforce HTTPS** once the certificate is issued (can take up to an hour).

## Editing later

All copy lives directly in `index.html` — open it, find the sentence, change it,
commit. Experience bullets are plain `<li>` items inside each `.role-body`.
Colors and fonts are the `:root` variables at the top of `styles.css`:
navy `#152A4E`, slate `#5A6A85`. Fonts load from Google Fonts — Cormorant Garamond
(headings), Barlow (body), Alex Brush (the R monogram only).
