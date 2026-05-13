# Rajesh K — Portfolio + JARVIS AI
**Engineering the Edge** · IoT · CPS · Embedded Systems

---

## Folder Structure

```
rajesh-portfolio/
├── index.html          ← Your complete portfolio (DO NOT rename)
├── api/
│   └── chat.js         ← Secure backend — holds your API key
├── vercel.json         ← Deployment config
├── package.json        ← Node project config
├── .gitignore          ← Keeps secrets out of git
├── .env.example        ← Shows what env variable is needed
└── README.md           ← This file
```

---

## Deploy in 4 Steps

### Step 1 — Push to GitHub

```bash
# In this folder:
git init
git add .
git commit -m "Initial portfolio deploy"
git branch -M main
git remote add origin https://github.com/RAJESHKANIKKAISELVAM/rajesh-portfolio.git
git push -u origin main
```

> Create the repo at github.com first. Name it: `rajesh-portfolio` (Public)

---

### Step 2 — Deploy to Vercel (free)

1. Go to **vercel.com** → Sign up with GitHub
2. Click **"Add New Project"**
3. Import your `rajesh-portfolio` repository
4. Framework Preset → **Other**
5. Click **Deploy**

---

### Step 3 — Add Your API Key (CRITICAL)

Without this, JARVIS chat will not work.

1. In Vercel → your project → **Settings** tab
2. Left sidebar → **Environment Variables**
3. Add:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** your key from console.anthropic.com
   - **Environment:** Production + Preview + Development
4. Click **Save**
5. Go to **Deployments** → click the 3 dots → **Redeploy**

Get your API key at: **console.anthropic.com** → API Keys → Create Key

---

### Step 4 — Your Live URL

After deploy, Vercel gives you:
```
https://rajesh-portfolio.vercel.app
```

Or connect a custom domain in Vercel → Settings → Domains.

---

## Add to LinkedIn

1. LinkedIn profile → **"Add profile section"** → Featured → Add link
2. Paste your Vercel URL
3. Title: `Portfolio — Engineering the Edge`
4. Description: `IoT · CPS · Embedded Systems · Edge Intelligence`

Also add to:
- Contact info → Website → Portfolio
- About section → bottom of bio
- Resume PDF header

---

## Update Resume Download Button

Once you have the live URL:
1. Open `index.html`
2. Find: `Download Resume`
3. Replace `href="#"` with link to your resume PDF
4. Commit and push → Vercel auto-redeploys

---

## How JARVIS Chat Works

```
Visitor types → index.html → /api/chat (Vercel serverless) → Anthropic API → response
```

The API key never touches the browser. It lives only on Vercel's servers.

---

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS — no build step needed
- **Backend:** Vercel Serverless Function (Node.js)
- **AI:** Claude claude-sonnet-4-20250514 via Anthropic API
- **TTS:** Web Speech API (browser native)
- **STT:** Web Speech Recognition API (Chrome)
- **Hosting:** Vercel (free tier)

---

**Rajesh K** · rkanikkaiselvam@hawk.illinoistech.edu
