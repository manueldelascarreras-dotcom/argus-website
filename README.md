# ARGUS website

Landing site for ARGUS, the AI operating assistant for small and medium businesses.

**Live:** https://argus-ai-web.web.app

## What's here

- `index.html` — the whole site (HTML, CSS and JS in one file). Pages: Home, How it works, Radar, Pricing, Book a pilot (hash routes like `#/radar`).
- `assets/eye-880.webp`, `assets/eye-560.webp` — hero eye (desktop / phone sizes). `assets/eye-raw.png` is the full-quality original.
- `assets/*.woff2` — self-hosted variable fonts (Inter Tight, Inter).
- `firestore.rules` — the pilot form can only *create* entries in the `pilotRequests` collection; nobody can read them from the browser.
- `serve.js` — tiny local server with no dependencies.

## Run locally

```bash
node serve.js
```

Then open http://localhost:8000

## Deploy (Firebase project `argus-ai-web`)

```bash
firebase deploy --only hosting
firebase deploy --only firestore:rules
```

Pilot requests show up in the Firebase console under Firestore → `pilotRequests`.
