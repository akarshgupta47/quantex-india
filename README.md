# QuantEx India 🇮🇳 — Algorithmic Trading Terminal

A production-grade, visually premium algorithmic trading bot dashboard built for the **Indian market** (NSE · BSE · MCX). Features a dark glassmorphism UI, real-time simulated data, and all core trading bot modules.

## 🚀 Live Demo
> After deploying: `https://<your-username>.github.io/quantex-india/`

## ✨ Features

| Module | Description |
|---|---|
| 📊 Dashboard | NIFTY 50 live chart, portfolio metrics, active positions, market status |
| 🧠 Strategy Engine | EMA Crossover, RSI, MACD, Bollinger Bands, **Supertrend** |
| 🛡️ Risk Manager | Stop loss, take profit, lot size, SEBI margin display |
| ⚡ Executor | Start/Stop bot, real-time trade log, live console |
| 📈 Backtest | Equity curve, Sharpe ratio, win rate, max drawdown |
| 📉 Analytics | Monthly returns, win/loss distribution, key metrics |
| 🔔 Alerts | Real-time alert feed, EOD daily update simulator |
| ⚙️ Settings | Zerodha, Angel One, Upstox, Fyers, ICICI Breeze API config |

## 🇮🇳 India-Specific Adaptations
- All prices in **₹ (Indian Rupee)** with `en-IN` locale formatting
- **IST (Indian Standard Time)** clock, not UTC
- **NSE/BSE market hours**: 09:15 – 15:30 IST (live status indicator)
- **MCX Commodity** and **Currency Derivatives** market sessions
- Instruments: NIFTY 50, BANKNIFTY, SENSEX, RELIANCE, TCS, INFY, HDFC Bank, ITC
- **F&O lot size** input and SEBI margin calculation
- **STT (Securities Transaction Tax)** factored into PnL display
- **Supertrend** strategy (most popular in Indian retail algo trading)
- Supported brokers: Zerodha Kite, Angel One SmartAPI, Upstox, 5paisa, Fyers, ICICI Breeze
- F&O expiry reminders (Thursday settlement)
- SEBI compliance badge

## 📁 File Structure
```
quantex-india/
├── index.html          # Complete single-file application
├── README.md           # This file
└── .nojekyll           # Required for GitHub Pages
```

## 🛠️ Deploy to GitHub Pages (Step-by-Step)

### Method 1: GitHub Web UI (Easiest)
1. Go to [github.com](https://github.com) → **New Repository**
2. Name it `quantex-india` → click **Create repository**
3. Click **uploading an existing file**
4. Drag and drop `index.html`, `README.md`, `.nojekyll`
5. Click **Commit changes**
6. Go to **Settings → Pages**
7. Under **Source**, select `main` branch → **Save**
8. Your site will be live at `https://<username>.github.io/quantex-india/` in ~2 minutes

### Method 2: Git CLI
```bash
git clone https://github.com/<your-username>/quantex-india.git
cd quantex-india
# Copy the files here
git add .
git commit -m "Initial deploy: QuantEx India Terminal"
git push origin main
```
Then enable GitHub Pages in Settings → Pages → Source: main branch.

## 🔌 Connecting to Real APIs (Future)

### Zerodha Kite API
```javascript
// Replace mock data with:
const kite = new KiteConnect({ api_key: "YOUR_KEY" });
kite.getQuote(["NSE:NIFTY50"]).then(data => { /* update chart */ });
```

### Angel One SmartAPI
```javascript
const smart_api = new SmartConnect({ api_key: "YOUR_KEY" });
await smart_api.generateSession(clientCode, password, totp);
```

## ⚠️ Disclaimer
This is a **simulation tool** for educational and demonstration purposes. It does **not** execute real trades. Always consult a SEBI-registered advisor before algorithmic trading. Paper trading mode is the default and recommended for testing.

---
**Built by Akarsh Kumar Gupta** · QuantEx India v2.4.1
