# Petsama — Home Pet Sitting in Bengaluru

Stay. Play. Be Loved. 🐾

A 3-page static site: `index.html` (home), `pricing.html`, `book.html`.
No build step, no framework — plain HTML/CSS/JS. Free to host on Vercel.

## Publish it — GitHub + Vercel (free), step by step

### 1. Create the GitHub repo
1. Go to [github.com/new](https://github.com/new)
2. Repository name: `petsama-website` (or anything you like)
3. Keep it **Public**, don't add a README/gitignore (we already have one)
4. Click **Create repository**

### 2. Push this folder to GitHub
Open a terminal in this folder and run:
```bash
git init
git add .
git commit -m "Initial Petsama site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/petsama-website.git
git push -u origin main
```
Replace `YOUR-USERNAME` with your actual GitHub username. If asked to log in,
GitHub will prompt you to authenticate (browser login or a personal access
token — GitHub will guide you through it).

### 3. Deploy on Vercel (free)
1. Go to [vercel.com](https://vercel.com) and sign up/log in **with your GitHub account**
2. Click **Add New → Project**
3. Select your `petsama-website` repo and click **Import**
4. Framework Preset: choose **Other** (it's a static site, no build needed)
5. Leave Build Command and Output Directory blank
6. Click **Deploy**

That's it — Vercel gives you a live URL like `petsama-website.vercel.app`
within about a minute.

### 4. Point your own domain (optional)
If you buy a domain (e.g. `petsama.in`) later:
1. In the Vercel project → **Settings → Domains** → add your domain
2. Vercel shows you DNS records to add at your domain registrar
3. Once DNS propagates (a few minutes to a few hours), your site is live on
   your own domain, still free on Vercel's side

### Updating the site later
Any time you edit a file and push to GitHub (`git add . && git commit -m "update" && git push`),
Vercel automatically redeploys. No manual steps needed after the first setup.

## File structure
```
petsama-site/
├── index.html          → home page
├── pricing.html        → pricing page
├── book.html           → booking form + WhatsApp
├── assets/
│   ├── petsama-logo.png
│   ├── petsama-banner.png   → used as social preview (og:image) + on-page banner
│   ├── favicon-32.png
│   └── apple-touch-icon.png
└── README.md
```

## Before you consider it fully "done"
- The booking form (`book.html`) currently shows a success message but does
  **not** send data anywhere yet. Bookings won't reach you until this is
  wired to a Google Sheet, email, or a small backend.
- WhatsApp number is hardcoded as `919996999505` in a few places — search
  and replace if it changes.
- Pricing figures in `pricing.html` are a starting point — confirm against
  real costs before treating them as final.
