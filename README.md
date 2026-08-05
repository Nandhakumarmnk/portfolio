# Nandhakumar M — Portfolio

Personal portfolio site for **Nandhakumar M**, Senior .NET Full-Stack Developer & Technical Lead.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire site — HTML, CSS, and JS in one self-contained file. No build step, no dependencies. |
| `Nandhakumar_M_Resume.pdf` | Résumé served by the "Download Résumé" buttons. Replace this file to update the download. |

## Run locally

Just double-click `index.html`. It works straight from the filesystem — there is no server requirement.

## Deploy to GitHub Pages

This gives you a free public URL like `https://<username>.github.io/portfolio`.

```bash
cd D:/Resume/portfolio
git init
git add .
git commit -m "Add portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/portfolio.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Source: `main` / `(root)` → Save**. The site is live in about a minute.

To publish at `https://<username>.github.io` instead (no `/portfolio` suffix), name the repository
`<your-username>.github.io` and push the same way.

Alternative one-step hosts: drag this folder onto [netlify.com/drop](https://app.netlify.com/drop),
or run `npx vercel` inside it.

## Updating content

Everything is plain HTML — edit `index.html` directly.

- **Hero stats** — the `data-count` and `data-suffix` attributes drive the animated counters.
  `data-count="500" data-suffix="+"` renders as `500+`.
- **Projects** — copy an entire `<article class="proj">` block to add another.
  Add `class="proj feature"` to make one span the full row.
- **Skills** — each `<div class="skill-card">` is one category; `<span class="tag">` is one chip.
- **Experience** — each `<div class="tl-item">` is one timeline entry.
- **Contact links** — in the `#contact` section. Update the `mailto:`, `tel:`, and LinkedIn `href`s together
  with their visible label text.

## Notes

- **Theme** — dark by default, with a light toggle in the navbar. The choice persists in `localStorage`
  and falls back to the visitor's OS preference on first visit.
- **Self-contained** — no CDN, no external fonts, no analytics. It renders offline and cannot break
  because a third party went down.
- **Responsive** — verified with no horizontal overflow down to a 360px viewport.
- **Accessibility** — honours `prefers-reduced-motion`; all animation is disabled for visitors who ask for that.
- **Printable** — `Ctrl+P` produces a clean document; navigation, buttons, and background effects are hidden.

## Suggested additions

The site has no GitHub link because there was no public repository to point at. If you create one,
add it to the `.contact-links` block in the `#contact` section and to the hero. A professional photo
in the hero and any certifications you hold would both strengthen the page further.
