# Site Map Generator (GitHub Pages)

Static web app for generating a `site.html`-style page from a pasted list of URLs.

## Use
1. Open `index.html` (locally or via GitHub Pages).
2. Paste one URL per line.
3. Optionally set page title and canonical URL.
4. Click **Generate**, then **Download site.html** or **Copy HTML**.

## Deploy on GitHub Pages
1. Push this repository to GitHub.
2. In repository settings, enable GitHub Pages for the desired branch/root.
3. Open the published `index.html`, generate output, and download/commit the resulting `site.html` as needed.

## Notes
- The generator inserts each pasted URL as an `<a href="...">` item (matching the existing `site.html` structure).
- Link labels are derived from each URL path/query.
- Existing `site.html` in this folder is left unchanged.
