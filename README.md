# Volcano Contours

A minimal static site ready for GitHub Pages. Use it to showcase volcano contour maps, notebooks, or project documentation.

## GitHub Pages deployment

1. Open **Settings → Pages** in the repository and set **Source** to **GitHub Actions**.
2. Push commits to the `work` branch. The included workflow `.github/workflows/pages.yml` builds and publishes the repository contents.
3. Watch the **Deploy GitHub Pages** workflow in the Actions tab. The public URL is printed in the deployment summary and on the Pages settings page.

### Customizing the site

- Edit `index.html` to change the layout or add additional sections.
- Update `assets/style.css` to adjust typography, colors, or spacing.
- If you need to publish from another branch or folder, change the `on.push.branches` and `upload-pages-artifact` `path` values in `.github/workflows/pages.yml`.

## Local preview

Because the site is static, you can open `index.html` directly in a browser. If you prefer a local server, run:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.
