# 🌿 The Olives Ministries — Website

## Files
- `index.html` — Main public website
- `admin.html` — CMS admin panel (access at `/admin`)
- `vercel.json` — Vercel routing config

## 🚀 Deploy to Vercel

### Option A — Drag & Drop (Easiest)
1. Go to [vercel.com](https://vercel.com) and sign in (free account)
2. Click **"Add New Project"**
3. Choose **"Deploy from your computer"** or drag this folder
4. Click **Deploy** — done! ✅

### Option B — Via GitHub (Recommended)
1. Create a free GitHub account at github.com
2. Create a new repository (e.g. `olives-ministries`)
3. Upload these 3 files: `index.html`, `admin.html`, `vercel.json`
4. Go to [vercel.com](https://vercel.com) → **Add New Project**
5. Import your GitHub repo → Deploy
6. Every time you update files on GitHub, Vercel auto-redeploys ✅

## 🔑 After Deploying

### Update Webhook URLs
In `admin.html`, replace `your-domain.vercel.app` with your actual Vercel URL in:
- Stripe webhook: `https://YOUR-SITE.vercel.app/api/stripe-webhook`
- M-Pesa callback: `https://YOUR-SITE.vercel.app/api/mpesa-callback`

### Admin Login
- URL: `https://your-site.vercel.app/admin`
- Username: `admin`
- Password: `olives2025`
- **Change the password** by editing line ~260 in `admin.html`

## 💳 Payment Integration Notes
The CMS stores your API keys locally in the browser. For full payment processing you will need a small backend (Vercel Serverless Functions work great — free tier). Contact a developer to wire up the Stripe and M-Pesa APIs once the site is live.
