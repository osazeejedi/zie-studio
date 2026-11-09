# ZIE Innovation Studio — Website

Marketing site + built-in shop for ZIE Innovation Studio (Abuja, Nigeria). Built with **React 18 + Vite 5**.

## Quick start

```bash
npm install
npm run dev        # http://localhost:5173
npm run build      # production build in dist/
npm run preview    # preview the built site
```

## Configure

All content lives inside `src/ZIEStudio.jsx` at the top of the file. Edit these constants:

| Constant | What it does |
|---|---|
| `WHATSAPP_NUMBER` | WhatsApp number (digits only, with country code). Used by every CTA. |
| `PHONE_DISPLAY` | Pretty phone shown in the footer. |
| `INSTAGRAM`, `EMAIL` | Contact links. |
| `SHOP_URL` | External shop (e.g. Bumpa). Empty = use the built-in shop. |
| `PROFILE_URL` | Path to your company profile PDF (keep it in `/public`). |
| `ANNOUNCEMENT` | Top banner text. Empty = hidden. |
| `PROJECTS` | Work gallery. Add image URLs per project. |
| `PRODUCTS` | Shop items. Set `price: null` to show "Price coming soon". |
| `DELIVERY_OPTIONS` | Checkout delivery options. `fee: null` disables online pay for that option. |
| `PAYSTACK_PUBLIC_KEY` | Your Paystack **public** key (`pk_live_…`). Empty = demo checkout. |

Drop your company profile PDF into `public/` using the filename referenced by `PROFILE_URL`.

## Deploy

**Vercel / Netlify** — framework: *Vite*, build command: `npm run build`, output: `dist`.
**GitHub Pages** — set `base: '/<repo>/'` in `vite.config.js`, then publish `dist/`.

## Stack
- React 18, Vite 5
- No CSS framework — all styles are scoped inside the component (`<style>` block using Inter Tight + Caveat from Google Fonts)
- Paystack Inline script is loaded on demand only when checkout is reached
