# GenZ Web — genz.ltd

Static marketing site for Stripe merchant review and USD subscription positioning.

**Brand:** GenZ · **Product:** PlanetX · **Tagline:** AI Career Growth Partner  
**Legal Entity:** YEDALL LIMITED  
**Deploy:** Vercel → genz.ltd

## Pages

| URL | File |
|-----|------|
| `/` | `index.html` |
| `/pricing` | `pricing.html` |
| `/legal/privacy` | `legal/privacy.html` |
| `/legal/terms` | `legal/terms.html` |
| `/legal/refund` | `legal/refund.html` |

URL rewrites configured in `vercel.json`.

## Vercel deploy

1. Import this repo on Vercel
2. Framework Preset: **Other**
3. Root Directory: `./` (repo root)
4. Build Command: leave empty
5. Output Directory: leave empty
6. Deploy

Bind `genz.ltd` and `www.genz.ltd` in Project Settings → Domains.

## Config

All site-wide config lives in `assets/config.js`:

```js
window.GENZ_SITE = {
  legalEntityName: "YEDALL LIMITED",
  brandName: "GenZ",
  productName: "PlanetX",
  tagline: "AI Career Growth Partner",
  supportEmail: "support@genz.ltd",
  siteUrl: "https://genz.ltd",
  apiBase: "https://api.genz.ltd",
};
```

## Pricing

Pricing loads dynamically from `api.genz.ltd/v1/payment/plans?region=US` with fallback to static defaults.

| Tier | Price | Stripe fee (3.4% + HK$2.35) | Net |
|------|-------|------|-----|
| Free | $0 | — | — |
| Supporter | $1.99/mo | ~$0.37 | $1.62 |
| Pro | $5.99/mo | ~$0.50 | $5.49 |

> Supporter fee ratio is ~18%. Consider raising to $4.99+ or going Free → Pro only.

## Source

Extracted from [looma-zervi](https://github.com/szpeter2026/looma-zervi) `frontend/packages/genz-web` for independent Vercel deployment.
