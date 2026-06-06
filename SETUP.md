# Guardian Codex — Setup Guide

## What you have
- `guardian-codex.html` — the frontend (GitHub Pages)
- `worker.js` — the Cloudflare Worker proxy code (already deployed)
- `SETUP.md` — this guide

---

## Step 1 — Cloudflare Worker (already done ✅)
Your Worker is live at:
```
https://guardian-codex.shamelessson.workers.dev
```
The frontend is already wired to this URL. Nothing to change here.

---

## Step 2 — Deploy to GitHub Pages

1. Go to github.com → create a **New Repository** (e.g. `guardian-codex`)
2. Set it to **Public**
3. Upload `guardian-codex.html` into the repo root
4. Go to **Settings → Pages**
5. Under Source → select **Deploy from a branch** → `main` → `/ (root)`
6. Click **Save**
7. Wait ~60 seconds → your site is live at:
   ```
   https://YOURUSERNAME.github.io/guardian-codex/guardian-codex.html
   ```

---

## Step 3 — Test it
1. Open your GitHub Pages URL
2. Type any X username (e.g. `solflare_wallet`)
3. Hit **Scan Guardian**
4. The full profile, stats, and strength breakdown appear automatically

---

## Troubleshooting

| Problem | Fix |
|---|---|
| "Could not load profile" | Check your twitterapi.io API key is correct in the Worker |
| Profile shows but bio is empty | That user has no bio set on X |
| CORS error in console | Make sure Worker has `Access-Control-Allow-Origin: *` |
| 401 from Worker | Your twitterapi.io key is wrong or expired |

---

## Credits used per scan
- 1 credit per Guardian scan (profile lookup)
- You have 10,000 free credits = 10,000 free scans
