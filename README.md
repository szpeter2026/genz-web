# GenZ Web — genz.ltd

**Stack:** Vite + React + `react-i18next` (English / 中文)  
**Brand:** GenZ · **Product:** PlanetX  
**Legal Entity:** YEDALL LIMITED  
**Deploy:** Vercel → `genz.ltd` / `www.genz.ltd`

Marketing SPA for Stripe merchant review and USD subscription positioning.

## i18n

- Locales: `src/i18n/locales/en.json`, `zh.json`
- Language switcher in header (persists to `localStorage` key `genz_lang`)
- Default: browser language (`zh*` → 中文, else English)

## Routes

| URL | Page |
|-----|------|
| `/` | Home |
| `/pricing` | Pricing |
| `/legal/privacy` | Privacy |
| `/legal/terms` | Terms |
| `/legal/refund` | Refund |

Legacy `.html` paths redirect to SPA routes.

## Local dev

```bash
npm install
npm run dev
# http://localhost:5180
```

## Vercel deploy

1. Import this repo on Vercel
2. Framework Preset: **Vite**
3. Build Command: `npm run build`
4. Output Directory: `dist`
5. Bind `genz.ltd` and `www.genz.ltd` in Project Settings → Domains

Push to `main` triggers automatic deployment.

## Config

Site-wide config: `src/config/site.ts` → `legalEntityName`, `apiBase`, etc.

## Source

Synced from [looma-zervi](https://github.com/szpeter2026/looma-zervi) `frontend/packages/genz-web` (`release/overseas`).
