# Alex Doe — Portfolio (test build)

A minimal static portfolio site, replicated from a Variant.com template. Plain HTML/CSS/JS — no build step, no dependencies beyond a Google Font.

## Files

```
index.html   — page structure & content
style.css    — all styling
script.js    — mobile nav toggle
```

## Preview locally

Just open `index.html` in a browser. Or, for a local server (handles relative paths identically to GitHub Pages):

```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Host it on GitHub Pages

1. Create a new repo on GitHub (e.g. `portfolio`).
2. Add these three files to the repo root (drag-and-drop on github.com works, or:
   ```bash
   git init
   git add .
   git commit -m "initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source → Deploy from a branch → main / (root)** → Save.
4. Your site goes live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## What's placeholder right now

- The 4 project thumbnails are just flat gray boxes with an icon — swap them for real images.
- Project titles/categories/years, the about paragraph, and contact info are all filler text.
- Email and social links in the contact section are dummy links.

## Replacing placeholders with your real images

Put your images in an `assets/` folder, then in `index.html` swap a block like this:

```html
<div class="project-thumb ph-1">
  <svg ...>...</svg>
</div>
```

for:

```html
<div class="project-thumb">
  <img src="assets/project-01.jpg" alt="Digital Ecosystem 01" />
</div>
```

and add this to `style.css` if not already covered:

```css
.project-thumb img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```
