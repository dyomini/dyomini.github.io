# dyomini.github.io

Personal homepage of Dongmin Yu. Plain HTML/CSS — no build step.
Design based on [Minimal Light](https://github.com/yaoyao-liu/minimal-light) (CC0).

## Structure

```
index.html                 all page content
assets/css/style.css       styles (light/dark mode follows the OS)
assets/img/profile.jpg     profile photo
assets/img/pub/            publication teaser images
files/                     CV and paper PDFs
.nojekyll                  tells GitHub Pages to serve files as-is
```

## Common edits

- **Photo**: replace `assets/img/profile.jpg` (square, ~480px).
- **CV**: in Overleaf, set `\publictrue` (hides phone and mailing address), recompile, download,
  save as `files/CV_DongminYu.pdf`, then set `\publicfalse` again.
- **News / publications**: copy an existing `<li>` in `index.html` and edit it.
- **Google Scholar / LinkedIn**: uncomment the matching line under `social-icons`.

## Cache busting

After editing `assets/css/style.css`, bump the `?v=` date on its `<link>` in `index.html`
so visitors' browsers load the new file instead of a cached copy.

## Preview locally

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Deploy to GitHub Pages

1. Create a public repository named `dyomini.github.io`.
2. Push these files to its `main` branch.
3. In the repo, go to Settings → Pages and choose "Deploy from a branch", `main`, `/ (root)`.
4. The site will be live at https://dyomini.github.io within a minute or two.
