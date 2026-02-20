# 📊 Market Trend Detector TradingView Pine Script

![Pine Script](https://img.shields.io/badge/Pine%20Script-v5-blue)
![TradingView](https://img.shields.io/badge/Platform-TradingView-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Free](https://img.shields.io/badge/Price-Free-success)

A powerful, all-in-one TradingView indicator combining **Market Trend Detection** and **Liquidity Sweep Detection** into a clean, real-time dashboard — built for price action and smart money traders.

---

## 🖼️ Preview
<img width="1920" height="927" alt="indicator" src="https://github.com/user-attachments/assets/ade7685f-3802-450d-9128-8515dc3df67d" />

> 

---

## 🚀 Features

### 📈 Market Trend Detector
- **4-Signal Scoring System** — scores market from 0–4 bull or bear
- **Live On-Screen Table** — stays fixed while panning/scrolling
- **EMA 20 / 50 / 200** — multi-timeframe trend layers
- **Supertrend Line** — dynamic support/resistance trailing line
- **Trend Cloud** — visual fill between EMA 20 and EMA 50
- **BUY / SELL Flip Markers** — when supertrend changes direction
- **Bar Coloring** — bars colored by trend strength
- **Adjustable Table Size** — Tiny / Small / Normal / Large / Huge
- **Adjustable Table Position** — Top Right / Left / Bottom Right / Left
- **Built-in Alerts** — for trend flips and strong trend confirmations

---

## 📥 Installation

1. Open [TradingView](https://www.tradingview.com)
2. Click on **Pine Script Editor** at the bottom of the chart
3. Delete any existing code
4. Copy and paste the script from either:
   - [`market_trend_detector.pine`](./market_trend_detector.pine)
   - [`liquidity_sweep.pine`](./liquidity_sweep.pine)
5. Click **Add to Chart**
6. Adjust settings from the indicator panel ⚙️

---

## ⚙️ Settings Guide

### Market Trend Detector

| Setting | Default | Description |
|---|---|---|
| Fast EMA | 20 | Short-term trend EMA |
| Slow EMA | 50 | Medium-term trend EMA |
| Trend EMA | 200 | Long-term trend direction |
| ATR Length | 14 | Period for Supertrend calculation |
| ATR Multiplier | 2.0 | Sensitivity of Supertrend line |
| Show EMAs | On | Toggle EMA lines |
| Show Trend Cloud | On | Toggle cloud fill between EMAs |
| Color Bars by Trend | On | Toggle bar coloring |
| Show Supertrend | On | Toggle supertrend line |
| Show Trend Table | On | Toggle on-screen dashboard |
| Table Position | Top Right | Move table to any corner |
| Table Text Size | Normal | Tiny / Small / Normal / Large / Huge |

---

## 📖 How To Use

### Reading the Trend Table

The table scores **4 signals** in real time:

| Signal | Bullish When |
|---|---|
| ● Price > EMA 200 | Price is above the 200 EMA |
| ● EMA20 > EMA50 | Fast EMA is above slow EMA |
| ● Supertrend Bull | Supertrend line is below price |
| ● Price > EMA20 | Price is above the fast EMA |

| Score | Status | Action |
|---|---|---|
| 4/4 Bull 🟢🟢🟢🟢 | Strong Uptrend | Look for BUY setups |
| 3/4 Bull 🟢🟢🟢🔴 | Weak Uptrend | Wait for confirmation |
| 2/4 Mixed 🟡🟡🟡🟡 | Sideways | Stay out |
| 3/4 Bear 🔴🔴🔴🟢 | Weak Downtrend | Avoid longs |
| 4/4 Bear 🔴🔴🔴🔴 | Strong Downtrend | Look for SHORT or stay flat |

---

### ✅ Trading Checklist
```
Step 1 → Check the Trend Table
         4/4 Bull = Only look for BUY setups
         4/4 Bear = Only look for SHORT setups
         2/4      = Do nothing

Step 2 → Check price vs EMA 200 (purple line)
         Above = Bull market territory
         Below = Bear market territory

Step 3 → Wait for BUY or SELL marker (Supertrend flip)
         Confirms momentum changed after the sweep

Step 4 → Enter the trade
         Entry  : Pullback to EMA 20 or Supertrend line
         Stop   : Below the Supertrend line or swing low
         Target : Previous swing high/low or 1:2 Risk/Reward

Step 5 → Exit when table flips direction
         or a SELL marker appears (for longs)
```

---

## 🏆 Best Practices

**Multi-Timeframe Analysis**
- Check **1H or 4H** for the overall trend (table score)
- Drop to **15M or 5M** for entries after a liquidity sweep
- If both timeframes agree → highest probability setup


**Avoid These Mistakes**
- ❌ Never trade against a 4/4 trend signal
- ❌ Never enter on a sweep alone — wait for the close confirmation
- ❌ Don't trade in 2/4 sideways markets
- ❌ Don't ignore the EMA 200 — it defines the macro trend

---

## 🔔 Setting Up Alerts

1. Right-click on the chart → **Add Alert**
2. In the **Condition** dropdown, select the indicator
3. Choose from available alerts:
   - `Trend Flipped Bullish`
   - `Trend Flipped Bearish`
   - `Strong Uptrend Active`
   - `Strong Downtrend Active`
   - `Buyside Liquidity Sweep`
   - `Sellside Liquidity Sweep`
4. Set notification method (app, email, webhook)
5. Click **Create**

---

## 📁 Files
```
📦 market-trend-liquidity-sweep
 ┣ 📄 market_trend_detector.pine   ← Main trend indicator
 ┣ 📄 liquidity_sweep.pine         ← Liquidity sweep indicator
 ┣ 📄 README.md                    ← This file
 ┗ 📄 LICENSE                      ← MIT License
```

---

## 🤝 Contributing

Pull requests are welcome! If you find a bug or want to suggest a feature:

1. Fork the repo
2. Create a new branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

---

## ⚠️ Disclaimer

> This indicator is for **educational purposes only**. It does not constitute financial advice. Trading involves significant risk of loss. Always do your own research and use proper risk management. Past performance does not guarantee future results.

---

## 📜 License

MIT License — free to use, modify, and distribute with attribution.

---

## ⭐ Support

If this helped you, please **star the repository** — it helps others find it!

> Built with ❤️ using Pine Script v5
