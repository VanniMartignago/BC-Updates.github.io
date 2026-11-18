# Business Central Updates

Bilingual, searchable feature archive for Microsoft Dynamics 365 Business Central.

## Files

- `index.html` contains the site interface and logic.
- `Business_Central_Updates.json` is the feature database loaded by the page.

The site supports Italian and English, free-text search, dependent major/minor release filters, area filters, newest-first ordering, and feature details with official Microsoft documentation links.

## Preview locally

Run a local web server from this folder (the page fetches the JSON file):

```sh
python -m http.server 8000
```

Then open `http://localhost:8000`.

## GitHub Pages

To host this repository with GitHub Pages, choose the `main` branch and repository root in the repository's Pages settings. The repository can also be cloned and served by any static hosting provider.

Live Sites version: https://bc.history.vanni-martignago.chatgpt.site/
