# TRT LabOS — trtlabos.com

Marketing site + app prototype for TRT LabOS.

## What's in this repo

- `index.html` — The full site (marketing landing page, lab panels, pricing, dashboard, onboarding). All pages are in a single file using JS-driven navigation.
- `netlify.toml` — Netlify configuration (redirects all routes to index.html)

## Local development

No build tools needed. Just open `index.html` in your browser, or run a local server:

```bash
# Option 1: Python (built into macOS/Linux)
python3 -m http.server 3000

# Option 2: VS Code Live Server extension
# Right-click index.html → "Open with Live Server"
```

## Deploying to Netlify (automatic)

1. Push changes to GitHub (main branch)
2. Netlify auto-deploys within ~30 seconds
3. Live at trtlabos.com

## Making changes

All content, styles, and logic are in `index.html`.

### Key sections to update:
- **Hero headline/subhead** — search for `hero-content` 
- **Pricing numbers** — search for `pro-price`, `clin-price`
- **Testimonials** — search for `testi-card` (replace placeholder quotes with real ones)
- **Biomarkers** — search for `bm-pill`
- **Clinic email** — replace `clinics@trtlabos.com` with your actual email
- **Contact email** — replace `hello@trtlabos.com` with your actual email

## GitHub → Netlify workflow

```
Edit in VS Code → git add . → git commit -m "what you changed" → git push → auto-deploys
```

## Domain setup (GoDaddy → Netlify)

1. In Netlify: Site Settings → Domain Management → Add custom domain → trtlabos.com
2. Copy the two Netlify nameservers
3. In GoDaddy: DNS → Nameservers → Custom → paste Netlify nameservers
4. Wait 10–60 minutes for DNS propagation
5. Netlify auto-provisions SSL (https) once DNS is live
