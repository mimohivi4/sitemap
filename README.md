# Site Map Generator (GitHub Pages)

Static web app for generating a `site.html`-style page from a pasted list of target URLs.

## How it works
- Paste one target URL per line (e.g. `https://postelniymir.ru/...`).
- Each pasted URL is inserted into the next link wrapper/template from the existing Site Resource Map, in order:
  - link 1 -> `http://secondary.lccsmobile.com/action/clickthru?targetUrl=<url1>`
  - link 2 -> `http://mailalpn.com/bitrix/redirect.php?goto=<url2>`
  - link 3 -> `https://ak38.ru/bitrix/redirect.php?goto=<url3>`
  - etc., preserving each wrapper's original form/encoding.
- If you paste more URLs than templates, templates cycle from the start.
- Link labels are derived from the pasted target URL path/query.

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
