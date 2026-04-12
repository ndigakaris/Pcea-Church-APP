# PCEA Registry — Frontend (Vercel)

Static HTML/CSS/JS frontend. Deploy this to **Vercel**.

## Before Deploying

Open `index.html` and update line ~490:

```js
const RAILWAY_API_URL = 'https://YOUR-RAILWAY-APP.up.railway.app';
```

Replace with your actual Railway backend URL (e.g. `https://pcea-registry-api.up.railway.app`).

## Deploy to Vercel

### Option A — Vercel CLI (fastest)
```bash
npm install -g vercel
vercel login
vercel --prod
```

### Option B — GitHub + Vercel Dashboard
1. Push this folder to a GitHub repo
2. Go to [vercel.com](https://vercel.com) → New Project → Import repo
3. Framework Preset: **Other**
4. Root Directory: leave as `/` (or the folder name)
5. Click **Deploy**

No build step needed — it's plain static HTML.

## After Deploying

Copy your Vercel URL (e.g. `https://pcea-registry.vercel.app`) and:
1. Go to Railway → your backend service → Variables
2. Set `FRONTEND_URL = https://pcea-registry.vercel.app`
3. Railway will redeploy automatically — CORS is now configured correctly

## Local Development

Open `index.html` directly in a browser, or use VS Code Live Server.
The app auto-detects `localhost` and points to `http://localhost:3000/api`.
