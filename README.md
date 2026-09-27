# ForgeProp

**AI-assisted freelance proposal generator**  
Proposals that win clients. Written in under a minute.

## Status (2026-09-27)

MVP website + working generator shipped as static files.

- `index.html` — Marketing homepage
- `app.html` — Live proposal generator (rule-based structured output, free tier via localStorage)
- `privacy.html` / `terms.html` — Basic legal pages

## How to run locally

Open any file in a browser, or serve the folder:

```bash
npx serve .
# or
python3 -m http.server 8080
```

Then visit `http://localhost:3000` (or the port shown).

## Deploy ($0)

- This repo is ready for Vercel / Netlify / Cloudflare Pages (all free tiers)
- Connect the repo → deploy → live URL in minutes
- Point a custom domain when ready (optional)

No backend required for the current MVP. Generation is client-side structured templates.

## Next product steps

1. Replace rule-based generation with a real LLM call (OpenAI / Anthropic / open-source via free tier or paid API). Pass cost through usage limits.
2. Add Supabase (or equivalent free tier) for accounts + history.
3. Stripe Checkout for Pro ($19/mo).
4. PDF generation via proper library (html2pdf / jsPDF / server-side).
5. Custom branding upload for Pro.

## Business model

- Free: 5 proposals / month
- Pro: $19 / month (or $15 annual equivalent) — unlimited + branding + history + tracking

## Acquisition (organic first)

- Reddit / Indie Hackers / Twitter posts with real sample outputs
- Long-tail SEO pages: “AI proposal generator for freelancers”, “freelance proposal template [niche]”
- Product Hunt launch once accounts + real AI are live

## Owner workload target

- Launch week: high (content + outreach)
- After 50–100 users: moderate (support + content)
- At scale: low (automation + docs)

## Legal note

This is a legitimate product. Do not fabricate testimonials or revenue claims. Always disclose AI assistance where relevant.
