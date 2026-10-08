# ForgeProp

**AI-assisted freelance proposal generator**  
Proposals that win clients. Written in under a minute.

## Live product

| File | Purpose |
|------|---------|
| `index.html` | Marketing homepage + pricing |
| `app.html` | Working proposal generator |
| `success.html` | Post-Stripe checkout thank-you |
| `privacy.html` / `terms.html` | Legal |

## Pricing (locked in)

- **Free:** 1 proposal / month
- **Pro:** $24 / month
- **Pro yearly:** $19 / month equivalent ($228 / year)

## Run locally

```bash
cd forgeprop
python3 -m http.server 8080
# open http://127.0.0.1:8080
```

## Deploy (free)

### Vercel
1. Go to https://vercel.com/new
2. Import `jamesjesse8814/forgeprop`
3. Framework: Other · Build: none · Output: `.`
4. Deploy → live URL in ~30 seconds

### Netlify
1. https://app.netlify.com → Add site → Import from Git
2. Select this repo · Build command empty · Publish directory `.`
3. Deploy

Every push to `main` redeploys automatically after you connect the repo once.

## Stripe setup (required for paid upgrades)

1. Create a free account at https://stripe.com
2. **Products → Add product**
   - Name: `ForgeProp Pro`
   - Price 1: $24 USD / month (recurring)
   - Price 2: $228 USD / year (recurring)
3. For each price: **Create payment link**
4. Copy the two Payment Link URLs (`https://buy.stripe.com/...`)
5. On the live site, open browser console and run:

```js
localStorage.setItem('fp_stripe_monthly', 'https://buy.stripe.com/YOUR_MONTHLY_LINK');
localStorage.setItem('fp_stripe_yearly', 'https://buy.stripe.com/YOUR_YEARLY_LINK');
```

Or edit the `STRIPE` object in `index.html` and `app.html` and redeploy.

Optional: set Payment Link **After payment → redirect** to  
`https://YOUR-DOMAIN/success.html`

## How free tier works

Client-side `localStorage` key `forgeprop_free_used`.  
After 1 generation, the upgrade modal opens with Stripe checkout.

## Next product steps

1. Real LLM generation (OpenAI / Anthropic) via Vercel serverless function
2. Supabase auth + proposal history
3. Stripe webhooks to unlock Pro in localStorage / account
4. Custom branding upload for Pro

## Owner

Repo: https://github.com/jamesjesse8814/forgeprop  
Legitimate product. No fake testimonials or revenue claims.
