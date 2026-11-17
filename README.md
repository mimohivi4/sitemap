# Site Map Generator (GitHub Pages)

Static web app for generating a `site.html`-style page from a pasted list of target URLs.

## How it works
- Paste one target URL per line.
- Each pasted URL is inserted into the next link wrapper/template from the existing Site Resource Map, in order (wrappers and encodings preserved). Templates cycle if you paste more URLs than templates.
- Link `href` = wrapper + pasted target URL.
- Link text shows the last ID/value from the pasted URL (prefers `id` param; otherwise last query value/name or last path segment), e.g. `...&id=83723709` displays as `83723709`.

## Files
- `index.html` — generator UI (open locally or via GitHub Pages).
- `templates.js` — extracted wrapper templates from the existing `site.html` (500 links, used in order).
- `site.html` — existing map (left unchanged unless you replace it with generated output).

## Use
1. Open `index.html`.
2. Paste target URLs (one per line).
3. Optionally set page title and canonical URL.
4. Click **Generate**, then **Download site.html** or **Copy HTML**.

## Deploy on GitHub Pages
1. Push this repository to GitHub.
2. In repository settings, enable GitHub Pages for the desired branch/root.
3. Open the published `index.html`, generate output, and download/commit the resulting `site.html` as needed.
