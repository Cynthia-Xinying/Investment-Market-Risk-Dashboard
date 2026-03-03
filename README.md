# 📊 Investment Market Risk Dashboard

A lightweight, AI-powered market risk terminal that runs entirely in your browser. No backend, no database — just open it, enter your API key, and get a live 4-pillar risk assessment in under 2 minutes.

[![Netlify Status](https://api.netlify.com/api/v1/badges/your-badge-id/deploy-status)](https://app.netlify.com)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![HTML](https://img.shields.io/badge/Built%20with-HTML%2FJS-orange)

---

## 🚀 Live Demo

> 🔗 **[your-site-name.netlify.app](https://your-site-name.netlify.app)**  
> *(Replace with your actual Netlify URL)*

---

## 💡 What It Does

Every morning, instead of checking 5 different websites, open this dashboard, paste your Anthropic API key, and click **Analyze Now**. The AI will:

1. **Search the web in real time** for current market data
2. **Evaluate 4 risk pillars** in the correct order (oil → credit → breadth → earnings)
3. **Give you a plain-English verdict** with color-coded risk levels and an action item for each pillar

The whole process takes under 2 minutes.

---

## 🔍 The 4 Risk Pillars

| Pillar | What It Tracks | Key Signal |
|---|---|---|
| ⛽ **Oil Price** | WTI / Brent crude | Is WTI approaching / breaking $100? |
| 💳 **Credit Spread** | HY OAS (High Yield Option-Adjusted Spread) | Widening 3–5 days in a row = systemic stress |
| 📊 **Market Breadth** | SPY/QQQ, VIX, A/D line | Are only a few large-cap stocks carrying the index? |
| 📈 **EPS Revisions** | S&P 500 forward P/E, CY EPS estimates | Is full-year earnings growth being revised down? |

**Why this order?** Oil is an external shock (fastest moving), credit confirms whether stress is systemic, breadth shows internal market structure, and EPS revisions are the slowest-moving but most consequential variable for long-term valuation.

---

## 🛠 How to Use

### Prerequisites
- A free [Anthropic API key](https://console.anthropic.com) (`sk-ant-api03-...`)
- Any modern browser (no installation needed)

### Steps
1. Open the live site link above
2. Paste your Anthropic API key into the field at the top
3. Click **▶ Analyze Now**
4. Wait ~15 seconds while the AI searches live market data
5. Click any risk card to expand the full analysis + "what to watch next"

> **Privacy note:** Your API key is never stored. It lives only in your browser's memory and is cleared when you close the tab.

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML / CSS / JavaScript (single file) |
| AI Engine | Claude Sonnet (Anthropic API) with live web search |
| Hosting | Netlify (free tier) |
| Data | Real-time web search — no static data |

No frameworks. No build step. No server. The entire app is `index.html`.

---

## 💰 Cost Estimate

Each time you click "Analyze Now," the AI runs a web search + analysis. Approximate cost:

| Usage | Estimated Cost |
|---|---|
| 1 analysis/day | ~$0.01–0.03 per run |
| Daily use, 1 month | ~$0.30–$0.90/month |

You pay only for what you use via the Anthropic API. The Netlify hosting is free.

---

## 🗂 Project Structure

```
index.html      ← The entire app (HTML + CSS + JS in one file)
README.md       ← This file
```

---

## 🔧 Customization

Want to change the risk thresholds or add new pillars? Edit the `SYSTEM_PROMPT` constant inside `index.html`:

```javascript
const SYSTEM_PROMPT = `You are a senior macro risk analyst...`
```

You can modify what the AI searches for, change the JSON structure, or add new metrics (e.g., DXY dollar index, 10Y yield) by updating the prompt and rendering logic.

---

## 📦 Deploy Your Own Copy

1. Fork this repo
2. Go to [netlify.com](https://netlify.com) → New site → Import from GitHub
3. Select this repo, leave all settings default, click **Deploy**
4. Done — your own live URL in 60 seconds

---

## 📄 License

MIT — free to use, modify, and distribute.

---

*Built with [Claude](https://claude.ai) · Powered by the Anthropic API*
