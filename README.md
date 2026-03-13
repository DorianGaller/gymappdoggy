# IronRank PWA – Deployment Guide

## Deploying to Vercel (free, ~2 minutes)

### Option A — Drag & Drop (easiest, no account needed beyond free signup)

1. Go to https://vercel.com and sign up for free (GitHub/Google login)
2. On your dashboard click **"Add New… → Project"**
3. Choose **"Deploy from template"** → scroll down → click **"Browse all templates"**
   — OR — simply go to https://vercel.com/new
4. Click **"Continue with…"** then choose **"Import a folder"**
5. Drag the entire `ironrank-pwa` folder into the upload area
6. Click **Deploy** — done in ~30 seconds!
7. Vercel gives you a URL like `https://ironrank-abc123.vercel.app`

### Option B — GitHub (recommended for updates)

1. Create a free account at https://github.com
2. Create a new repository called `ironrank`
3. Upload all files from this folder to the repo
4. Go to https://vercel.com → New Project → Import from GitHub → select `ironrank`
5. Click Deploy
6. Every time you push changes to GitHub, Vercel auto-redeploys

---

## Installing on iPhone (iOS 16.4+)

1. Open Safari on your iPhone (must be Safari, not Chrome!)
2. Go to your Vercel URL (e.g. https://ironrank-abc123.vercel.app)
3. Tap the **Share button** (box with arrow pointing up) at the bottom
4. Scroll down and tap **"Add to Home Screen"**
5. Give it a name (e.g. "IronRank") → tap **Add**
6. The app icon appears on your home screen — tap it to open fullscreen!

---

## Data Storage

All your data (PRs, sessions, achievements) is stored in **localStorage** on your device.
- Data persists between app restarts ✅
- Data is private — never sent to any server ✅
- If you clear Safari's website data, your data will be lost ⚠️
  → Use Settings → Safari → Advanced → Website Data → Do NOT clear ironrank data

---

## Sharing your rank with friends

Just share your Vercel URL with friends so they can install it too!
Each person's data is stored separately on their own device.

---

## Project files

```
ironrank-pwa/
├── index.html      ← The entire app (React + all code inline)
├── manifest.json   ← PWA config (name, icons, theme)
├── sw.js           ← Service worker (offline support)
├── vercel.json     ← Vercel deployment config
├── icons/
│   ├── icon-180.png   ← Apple touch icon (home screen)
│   ├── icon-192.png   ← Android / PWA icon
│   └── icon-512.png   ← Large PWA icon
└── README.md       ← This file
```
