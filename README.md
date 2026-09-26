# Personal Website — Emmanuel Adjei Domfeh

A single-file, dependency-free personal academic website. No build step, no framework, no hosting cost.

## Files in this folder

| File | Purpose |
|---|---|
| `index.html` | The entire website — HTML, CSS, and JavaScript in one file |
| `cv.pdf` | Your CV, linked from the "Download CV" buttons |
| `photo.jpeg` | Your headshot (800×800), already wired into the page |

Everything is ready to publish — just upload all four files.

### Swapping the photo later

Drop a new square image into this folder and update the `src` on this line in `index.html`:

```html
<img src="photo.jpeg" alt="Portrait of Emmanuel Adjei Domfeh">
```

If the face sits too high or low inside the circle, adjust this rule in the `<style>` block:

```css
.portrait img{ transform:scale(1.14) translateY(3%); }
```

Increase `scale` to zoom in; make `translateY` more negative to move the image up.

## Publish free on GitHub Pages

**One-time setup, about 10 minutes.**

1. Create a free account at [github.com](https://github.com) if you don't have one.
2. Create a new repository named exactly:

   ```
   emmanueladjeidomfeh.github.io
   ```

   Replace `emmanueladjeidomfeh` with your actual GitHub username. The `.github.io` suffix is what makes it a personal site.

3. Set visibility to **Public**, then click **Create repository**.
4. On the new repo page, click **uploading an existing file**.
5. Drag in `index.html`, `cv.pdf`, and `photo.jpg`. Click **Commit changes**.
6. Go to **Settings → Pages**. Under "Branch", select `main` and `/ (root)`, then **Save**.
7. Wait 1–2 minutes. Your site is live at:

   ```
   https://emmanueladjeidomfeh.github.io
   ```

**To update later:** edit the file on GitHub directly (click the file, then the pencil icon), or re-upload. Changes go live within a minute.

### Custom domain (optional, ~$12/year)

If you buy a domain such as `adjeidomfeh.com`:

1. In **Settings → Pages → Custom domain**, enter your domain and save.
2. At your domain registrar, add these DNS records:
   - Four `A` records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` pointing to `emmanueladjeidomfeh.github.io`
3. Back in GitHub Pages settings, tick **Enforce HTTPS** once it becomes available.

## Alternative: Netlify (no GitHub account needed)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag this entire folder onto the page.
3. Your site is live instantly at a `*.netlify.app` address. Create a free account to keep it and rename the URL.

## Keeping the site current

The numbers most worth updating are in two places:

- **Citation metrics** — the `<div class="metrics">` block near the top (currently 102 citations, h-index 4)
- **Per-paper citation counts** — the `chip chip-cite` spans in the Publications section

Check your [Google Scholar profile](https://scholar.google.com/citations?user=QS6Mi14AAAAJ) every few months and update these. Add new publications by copying an existing `<div class="pub">` block and editing the contents.

## Technical notes

- Works in all modern browsers; degrades gracefully in older ones
- Fully responsive — tested at desktop (1440px) and mobile (390px) widths
- Respects `prefers-reduced-motion` for accessibility
- Fonts load from Google Fonts; everything else is self-contained
- Open Graph tags included, so links shared on LinkedIn or Twitter show a proper preview
