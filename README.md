# TRT LabOS — trtlabos.com

Full website for TRT LabOS with separate pages, shared stylesheet, and Netlify deployment.

## File structure

```
trtlabos-site/
├── index.html       → trtlabos.com/
├── panels.html      → trtlabos.com/panels
├── pricing.html     → trtlabos.com/pricing
├── dashboard.html   → trtlabos.com/dashboard
├── signup.html      → trtlabos.com/signup
├── styles.css       → shared styles across all pages
├── netlify.toml     → URL redirects (panels vs panels.html etc)
├── .gitignore
└── README.md
```

## Local development

No build tools needed. Open any HTML file directly in your browser, or use VS Code Live Server:
- Install the "Live Server" extension in VS Code
- Right-click any HTML file → "Open with Live Server"
- Navigation between pages works correctly on Live Server

## Making changes

### Shared across all pages (styles.css)
- Nav styles, button styles, footer, shared layout
- Change button colors here to update everywhere at once

### Page-specific content
- `index.html` — hero, pain/solution, stats, features, testimonials, clinic CTA
- `panels.html` — panel cards, biomarkers, cadence, differentiators
- `pricing.html` — billing toggle, plan cards, clinic band
- `dashboard.html` — metrics, AI insight, charts, lab panel, reminders
- `signup.html` — 4-step onboarding flow

### Things to update before real launch
1. Replace placeholder testimonials (search `testi-quote`) with real user quotes
2. Replace `clinics@trtlabos.com` and `hello@trtlabos.com` with real emails
3. Wire up the signup form to a real backend (Stripe, auth, etc.)
4. Add Google Analytics or Plausible for tracking

## Deploy to Netlify

Push to GitHub → Netlify auto-deploys on every push to main.

Clean URLs work via netlify.toml redirects:
- trtlabos.com/pricing → pricing.html
- trtlabos.com/panels → panels.html
- trtlabos.com/dashboard → dashboard.html
- trtlabos.com/signup → signup.html

## GitHub workflow

```bash
# After making changes in VS Code:
git add .
git commit -m "describe what you changed"
git push
# Netlify auto-deploys in ~30 seconds
```
