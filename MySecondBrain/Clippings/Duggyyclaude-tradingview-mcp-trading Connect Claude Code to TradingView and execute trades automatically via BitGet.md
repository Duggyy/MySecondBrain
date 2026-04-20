---
title: "Duggyy/claude-tradingview-mcp-trading: Connect Claude Code to TradingView and execute trades automatically via BitGet"
source: "https://github.com/Duggyy/claude-tradingview-mcp-trading"
author:
published:
created: 2026-04-20
description: "Connect Claude Code to TradingView and execute trades automatically via BitGet - Duggyy/claude-tradingview-mcp-trading"
tags:
  - "clippings"
---
## Claude + TradingView MCP — Automated Trading

> **New to this?** Watch the previous video first — it sets up the TradingView MCP connection this builds on.

[![How To Connect Claude to TradingView (Insanely Cool)](https://camo.githubusercontent.com/fd28be9f6133457352e008bbeb59ae496de228babd312e845e3091cfa367a96e/68747470733a2f2f696d672e796f75747562652e636f6d2f76692f764958367a74554c7334552f6d617872657364656661756c742e6a7067)](https://youtu.be/vIX6ztULs4U)

[![Claude Code + TradingView Now Actually Executes Real Trades](https://camo.githubusercontent.com/b531d2577eb65ada7ea13e9e995b18d0bfeab0f1d926752c4640e295a02ee1aa/68747470733a2f2f696d672e796f75747562652e636f6d2f76692f6144574a366c4c656d4a552f6d617872657364656661756c742e6a7067)](https://www.youtube.com/watch?v=aDWJ6lLemJU)

---

## What This Does

**Five things you get from this setup:**

1. **Claude connected to your exchange** — reads your TradingView chart and executes trades on BitGet automatically
2. **A safety check** — every condition in your strategy must pass before a single trade goes through
3. **24/7 cloud execution** — deploy to Railway and it runs on a schedule, even when your laptop is closed
4. **Automatic tax accounting** — every trade logged to `trades.csv` with date, price, fees, and net amount, ready for your accountant
5. **Free** — no email, no course, no upsell. Everything is in this repo.

---

## The One-Shot Prompt

> **This is the thing you paste.** Open Claude Code in this directory, paste the entire contents of [`prompts/02-one-shot-trade.md`](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/prompts/02-one-shot-trade.md), and Claude will do the rest.

Here's what it does when you run it:

| Step | What Claude does |
| --- | --- |
| 1 | Reads your `rules.json` strategy |
| 2 | Pulls live price + indicator data from TradingView |
| 3 | Calculates MACD from raw candle data |
| 4 | Evaluates market bias (bullish / bearish / neutral) |
| 4b | Checks trade limits — daily cap and max trade size |
| 5 | Runs the safety check — every entry condition checked |
| 6 | Executes the trade via BitGet if all conditions pass |
| 7 | Logs the trade to `trades.csv` — date, price, fees, net amount (tax-ready) |
| 8 | Saves full decision log to `safety-check-log.json` |

If anything fails the safety check, it stops and tells you exactly which condition failed and the actual values. No trade goes through unless everything lines up.

---

## Getting Started

### Step 1 — Paste the one-shot prompt into Claude Code

Copy the entire contents of [`prompts/02-one-shot-trade.md`](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/prompts/02-one-shot-trade.md) and paste it into your Claude Code terminal.

That's it. Claude acts as your onboarding agent — it clones the repo, walks you through connecting BitGet, sets your trading preferences, connects TradingView, optionally builds a strategy from a YouTube channel, deploys to Railway, and runs the bot for the first time. Every step is interactive. It pauses when it needs something from you and handles everything else automatically.

---

## What's Happening Under the Hood

For anyone who wants to understand the steps manually, or troubleshoot a specific part:

### Prerequisites

- **TradingView MCP** must already be set up — built in the [first video](https://youtu.be/vIX6ztULs4U)
- **Claude Code** installed and running
- **A BitGet account** — sign up here for a $1,000 bonus on your first deposit
- **Node.js 18+** — check with `node --version`

---

### Clone the repo

**Mac / Linux:**

```
git clone https://github.com/jackson-video-resources/claude-tradingview-mcp-trading
cd claude-tradingview-mcp-trading
```

**Windows:**

```
git clone https://github.com/jackson-video-resources/claude-tradingview-mcp-trading
cd claude-tradingview-mcp-trading
```

---

### Add your BitGet API credentials

**Mac / Linux:**

```
cp .env.example .env
```

**Windows:**

```
Copy-Item .env.example .env
```

Open `.env` and fill in:

```
BITGET_API_KEY=your_api_key_here
BITGET_SECRET_KEY=your_secret_key_here
BITGET_PASSPHRASE=your_passphrase_here
PORTFOLIO_VALUE_USD=1000
MAX_TRADE_SIZE_USD=100
MAX_TRADES_PER_DAY=3
```

**Getting your API key:**

Step-by-step guides for all supported exchanges:

| Exchange | Guide |
| --- | --- |
| BitGet *(used in the video)* | [docs/exchanges/bitget.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/bitget.md) |
| Binance | [docs/exchanges/binance.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/binance.md) |
| Bybit | [docs/exchanges/bybit.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/bybit.md) |
| OKX | [docs/exchanges/okx.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/okx.md) |
| Coinbase Advanced | [docs/exchanges/coinbase.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/coinbase.md) |
| Kraken | [docs/exchanges/kraken.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/kraken.md) |
| KuCoin | [docs/exchanges/kucoin.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/kucoin.md) |
| Gate.io | [docs/exchanges/gateio.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/gateio.md) |
| MEXC | [docs/exchanges/mexc.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/mexc.md) |
| Bitfinex | [docs/exchanges/bitfinex.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/exchanges/bitfinex.md) |

Two rules that apply to every exchange — **withdrawals OFF, IP whitelist ON**.

---

### Launch TradingView and connect the MCP

**Mac:**

```
tv_launch
tv_health_check
```

**Windows:** See [docs/setup-windows.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/setup-windows.md)

**Linux:** See [docs/setup-linux.md](https://github.com/Duggyy/claude-tradingview-mcp-trading/blob/main/docs/setup-linux.md)

Verify with `tv_health_check` — should return `cdp_connected: true`.

---

### Run the bot manually

```
node bot.js
```

---

## Deploy to Railway (Run in the Cloud 24/7)

The local setup runs when your laptop is open. Railway lets the bot check for setups around the clock — even while you sleep.

> **Note:** Cloud mode pulls candle data directly from Binance's free market API instead of TradingView. No TradingView Desktop needed in the cloud. The strategy logic and safety check are identical.

### 1\. Deploy

```
npm install -g @railway/cli
railway login
railway init
railway up
```

### 2\. Set your environment variables in Railway

Go to your Railway project → Variables and add everything from `.env.example`:

| Variable | Example |
| --- | --- |
| `BITGET_API_KEY` | your key |
| `BITGET_SECRET_KEY` | your secret |
| `BITGET_PASSPHRASE` | your passphrase |
| `PORTFOLIO_VALUE_USD` | 1000 |
| `MAX_TRADE_SIZE_USD` | 100 |
| `MAX_TRADES_PER_DAY` | 3 |
| `PAPER_TRADING` | true (set to false when ready) |
| `SYMBOL` | BTCUSDT |
| `TIMEFRAME` | 4H |

### 3\. Set a cron schedule

In Railway → Settings → Cron Schedule, set how often the bot runs. Recommended:

| Timeframe | Schedule | What it means |
| --- | --- | --- |
| 4H chart | `0 */4 * * *` | Every 4 hours |
| 1D chart | `0 9 * * *` | Once a day at 9am UTC |
| 1H chart | `0 * * * *` | Every hour |

### 4\. Start in paper trading mode

`PAPER_TRADING=true` logs every decision but never places real orders. Watch a few days of paper trades, confirm the logic matches what you expect, then flip it to `false`.

---

## Build Your Own Strategy (Optional)

The example `rules.json` uses the van de Poppe + Tone Vays BTC strategy. To build one from any trader's public videos:

1. Go to [Apify](https://apify.com/?fpr=3ly3yd) and search the actor store for **YouTube Transcript Scraper** — takes about 30 seconds per channel
2. Paste the output into `prompts/01-extract-strategy.md`
3. Run that prompt in Claude Code — it generates a `rules.json` tailored to that trader's methodology

---

## Files

| File | What it does |
| --- | --- |
| `rules.json` | Your strategy — indicators, entry rules, risk rules |
| `.env` | Your BitGet credentials (gitignored — never commits) |
| `prompts/01-extract-strategy.md` | Build rules.json from trader transcripts |
| `prompts/02-one-shot-trade.md` | **The one-shot prompt — paste this to trade** |
| `safety-check-log.json` | Auto-generated log of every trade decision |
| `trades.csv` | Tax-ready trade record — auto-written on every execution |
| `docs/setup-windows.md` | Windows-specific MCP setup |
| `docs/setup-linux.md` | Linux-specific MCP setup |

---

## Tax Accounting

Every trade the bot places is automatically written to `trades.csv` with the columns your accountant needs:

| Column | Description |
| --- | --- |
| Date | ISO date of the trade |
| Time | UTC time |
| Exchange | BitGet |
| Symbol | e.g. BTCUSDT |
| Side | Buy / Sell |
| Quantity | Units traded |
| Price | Price per unit at execution |
| Total USD | Gross trade value |
| Fee (est.) | Estimated exchange fee |
| Net Amount | Total USD minus fee |
| Order ID | Exchange reference |
| Mode | Paper / Live |

At tax time: open the file, hand it to your accountant, or import it directly into your accounting software. Nothing to reconstruct.

For a quick summary of your trading activity, run:

```
node bot.js --tax-summary
```

This prints total trades, volume, and fees paid.

---

## Safety

The safety check conditions are not fixed — they come directly from your `rules.json`. If you build a strategy from a YouTube trader's transcripts using the Apify prompt, your safety check will reflect that trader's entry logic. If you use the example strategy, it reflects those conditions. They're yours, not a generic filter.

Every condition in your `entry_rules` must pass before a trade goes through. One fails — nothing happens. The bot tells you exactly which condition failed and the actual value it saw.

Additional guardrails that apply regardless of strategy:

- Maximum trade size capped at `MAX_TRADE_SIZE_USD` in `.env`
- Maximum trades per day capped at `MAX_TRADES_PER_DAY` in `.env`
- Position sizing calculated from your portfolio value — max 1% risk per trade
- Every decision logged to `safety-check-log.json` with exact indicator values
- Every executed trade recorded in `trades.csv` for accounting

**This is not financial advice.** Build your strategy properly. Run the backtest. Paper trade before going live. Never put in more than you can afford to lose.

---

## Resources

- [First video — Connect Claude to TradingView](https://youtu.be/vIX6ztULs4U)
- [TradingView MCP repo (first video)](https://github.com/jackson-video-resources/tradingview-mcp-jackson)
- [Apify](https://apify.com/?fpr=3ly3yd) — search actor store for "YouTube Transcript Scraper"
- BitGet — $1,000 bonus on first deposit