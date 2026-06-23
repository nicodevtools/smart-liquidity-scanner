# 🔍 Smart Liquidity Scanner — Advanced TradingView Indicator

> **Detect institutional liquidity zones, Fair Value Gaps, and Order Blocks — like Smart Money traders do.**

[![Pine Script](https://img.shields.io/badge/Pine_Script-v5-00B295?style=flat-square&logo=tradingview&logoColor=white)](https://www.tradingview.com/pine-script-docs/)
[![TradingView](https://img.shields.io/badge/TradingView-Compatible-2196F3?style=flat-square&logo=tradingview)](https://www.tradingview.com)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=flat-square)](./LICENSE)
[![Version](https://img.shields.io/badge/Version-2.0-brightgreen?style=flat-square)](.)
[![Stars](https://img.shields.io/badge/⭐_Star_this_repo-if_useful-yellow?style=flat-square)](.)

<p align="center">
  <img src="https://img.shields.io/badge/%F0%9F%94%8D-FVG_Detection-7c3aed?style=for-the-badge" alt="FVG">
  <img src="https://img.shields.io/badge/%F0%9F%A7%B1-Order_Blocks-f59e0b?style=for-the-badge" alt="OB">
  <img src="https://img.shields.io/badge/%F0%9F%93%8A-Dynamic_S/R-10b981?style=for-the-badge" alt="SR">
  <img src="https://img.shields.io/badge/%F0%9F%9A%A8-Real_time_Alerts-ef4444?style=for-the-badge" alt="Alerts">
</p>

---

## 📖 Table of Contents
- [What Makes This Different](#-what-makes-this-different)
- [Features](#-features)
- [How To Install](#-how-to-install)
- [Strategy Guide](#-strategy-guide)
- [Settings & Configuration](#-settings--configuration)
- [PRO vs LITE](#-pro-vs-lite)
- [Pricing](#-pricing)
- [FAQ](#-faq)

---

## 🎯 What Makes This Different

Most liquidity indicators draw random lines and call them "zones." **This one uses real institutional concepts:**

| Concept | What It Detects | Why It Matters |
|---------|----------------|----------------|
| **FVG (Fair Value Gaps)** | Imbalance zones where price moved too fast | Price revisits ~70% of FVGs. High-probability entries. |
| **Order Blocks** | Bullish/Bearish OB with volume confirmation | Where institutions placed their orders |
| **Swing Liquidity** | Highs/lows with pending stop-loss orders | Stop hunts = liquidity grabs. Trade the reversal. |
| **Dynamic S/R** | Auto-calculated pivots | No more manual chart markup |

---

## ✨ Features

```pinescript
// Detects all this automatically:
✅ Fair Value Gaps (FVG) — BULLISH & BEARISH
✅ Order Blocks — with volume confirmation
✅ Liquidity Sweeps — stop-hunt detection
✅ Dynamic Support & Resistance — pivot-based
✅ Volume Profile integration
✅ Built-in dashboard overlay
✅ Real-time TradingView alerts (Telegram/Discord/Email)
✅ Multi-timeframe compatible (1M to 1W)
✅ Clean overlay — doesn't clutter your chart
```

## 📥 How To Install

1. Open **TradingView** → **Pine Editor** (bottom panel)
2. Copy the contents of `smart-liquidity-scanner.pine`
3. Paste into Pine Editor → Click **"Add to Chart"**
4. **Done.** Works instantly on any pair, any timeframe.

> 🆓 **Try the LITE version first:** [`smart-liquidity-scanner-lite.pine`](./smart-liquidity-scanner-lite.pine)

---

## 📈 Strategy Guide

### The FVG Fill Strategy
```
1. Wait for a strong impulsive move that leaves an FVG
2. Mark the FVG zone (indicator does this automatically)
3. Wait for price to retrace INTO the zone
4. Enter on the first reversal candle inside the zone
5. Stop loss: just beyond the FVG
6. Target: next liquidity level / opposite OB
```

### Order Block + FVG Confluence (High Probability)
```
When an Order Block overlaps with an FVG → 2x confirmation
This is where institutions have both:
  - Pending orders (OB)
  - Unfilled orders (FVG)
= Double reason for price to reverse
```

### Liquidity Sweep Reversal
```
1. Indicator marks a swing high/low
2. Price breaks it (stop hunt) — indicator labels "LIQ SWEEP"
3. Wait for price to reclaim the broken level
4. Enter in the direction of the reclaim
5. This is the classic "stop hunt → reversal" setup
```

---

## ⚙️ Settings & Configuration

| Setting | Default | Description | Recommendation |
|---------|---------|-------------|----------------|
| **Lookback Period** | 50 | Bars to analyze for swings | 30-50 (lower=faster) |
| **FVG Filter** | ON | Minimum gap size filter | ON for crypto, OFF for forex |
| **OB Strength** | Medium | Volume threshold for OB | Medium for most markets |
| **Volume Filter** | 1.5x | Min volume multiplier | 1.5x (pro only) |
| **Alert Types** | All | FVG/OB/Liquidity | Enable what you trade |

### Timeframe Combinations
```
👑 SWING TRADING:   4H (context) + 1H (entry) + 15M (precision)
📊 DAY TRADING:     1H (context) + 15M (entry) + 5M (precision)
⚡ SCALPING:        15M (context) + 5M (entry) + 1M (precision)
```

---

## 🆚 PRO vs LITE

| Feature | LITE (Free) | PRO |
|---------|:-----------:|:---:|
| Fair Value Gaps | ✅ | ✅ |
| Order Blocks | ✅ | ✅ |
| Swing Highs/Lows | ✅ | ✅ |
| **Volume Confirmation** | ❌ | ✅ |
| **Real-time Alerts** | ❌ | ✅ |
| **Liquidity Sweeps** | ❌ | ✅ |
| **Dynamic S/R** | ❌ | ✅ |
| **Dashboard Overlay** | ❌ | ✅ |
| **Custom Colors/Labels** | ❌ | ✅ |
| **Lifetime Updates** | — | ✅ |
| **Priority Support** | — | ✅ |

---

## 💰 Pricing

**Pay What You Want — Minimum $5 in Crypto**

| Payment Method | Network |
|:---:|:---:|
| 💎 **USDT** | Polygon |
| 🟣 **POL** | Polygon |
| ⟠ **ETH** | Polygon |

```
Wallet: 0xD404AE6B45Cae3D453D4408de99eC489Ce0fc18e
```

**After Payment:**
1. Send me your TX hash (via GitHub issue or DM)
2. Receive all source files + setup guide
3. Lifetime updates included

📦 **[Get Complete Bundle — 5 Tools for $15](https://github.com/nicodevtools/nico-trading-toolkit)**

---

## ❓ FAQ

**Q: Does this repaint?**
A: No. All signals use confirmed candle closes. Once a signal appears, it stays.

**Q: Works on crypto only?**
A: Works on ALL markets — Crypto, Forex, Stocks, Indices, Commodities.

**Q: What makes this better than free indicators?**
A: Volume confirmation eliminates false signals. Free indicators show everything; this filters noise.

**Q: Can I use it on multiple devices?**
A: Yes, single-user license covers all your devices.

**Q: I paid. How do I get the files?**
A: Open a GitHub issue with your TX hash. Files delivered within 24h (usually minutes).

---

## 🌐 More Free Tools by Nico

| Tool | Description | Link |
|------|-------------|------|
| 🧰 **CryptoKit Pro** | 6 free crypto tools (calculator, tracker, simulator) | [Try Now](https://nicodevtools.github.io/cryptokit-pro/) |
| 📊 **S/R Zone Pro** | Auto support/resistance zones | [View Repo](https://github.com/nicodevtools/sr-zone-pro) |
| 🔄 **Momentum Reversal Scanner** | RSI divergence + MACD + Volume | [View Repo](https://github.com/nicodevtools/momentum-reversal-scanner) |
| 🤖 **Crypto Sniper Bot** | DEX pair monitor | [View Repo](https://github.com/nicodevtools/crypto-sniper-bot) |
| ⚡ **Flash Arbitrage Scanner** | On-chain arb finder | [View Repo](https://github.com/nicodevtools/flash-arbitrage-scanner) |

---

## ⭐ Star This Repo

If this indicator helps your trading, drop a ⭐ — it helps others find it.

## 📣 Share This Tool

```
🔥 Just found the Smart Liquidity Scanner by @nicodevtools
— FVG + Order Blocks + Liquidity Zones, all auto-detected.
Free LITE version, PRO for $5+ crypto. 🎯
🔗 https://github.com/nicodevtools/smart-liquidity-scanner
```

---

<p align="center">
  <strong>Built by a trader. For traders. No BS.</strong><br>
  <sub>© Nico 🎯 — <a href="https://github.com/nicodevtools">github.com/nicodevtools</a></sub>
</p>
