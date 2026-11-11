# Mind Mart

A clickable prototype of a shop-style Mind builder: pick a Mind, equip skills, give app access, awaken.

## Run it

It is a static site. Open `index.html` in a browser, or host the folder as is
(GitHub Pages: Settings → Pages → deploy from the `main` branch, root folder).

## What is real and what is not

- **Real:** the 19 one-click Minds, 29 featured skills and 40 apps, with names and
  descriptions as shown on the Minds Bazaar in November 2026. Character and icon
  images are official Minds art, resized.
- **Placeholder:** the catalog is hardcoded in `index.html` (`MINDS`, `SKILLS`, `APPS`).
  Nothing calls the Minds API. "Best match" stars come from hand-written topic tags,
  power scores are invented, and "Awaken" creates nothing: it only builds a sample
  order (`template`, `name`, `skills`, `apps`) that you can copy.
- **Name:** "Mind Mart" is a working title.

## Wiring it to the Minds API

1. Replace the three arrays with responses from the catalog endpoints.
2. Send the order from "Awaken now" to the builder endpoint that creates a Mind.
3. Keep the API key on a server, not in this page: put a small backend or
   serverless function between the page and the API.
