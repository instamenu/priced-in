# 🤖 Priced In

An autonomous AI-powered stock trading agent that executes trades on GitHub Actions, built with OpenAI's Agents framework.

<!-- auto start -->

## 💰 Portfolio value: $855.31** (-97.64% CAGR)

### 📊 Holdings

| Asset | Shares | Value |
|-------|--------|-------|
| Cash | - | $0.01 |
| HLIT | 11 | $99.33 |
| ENVB | 63 | $69.30 |
| IMNN | 7 | $50.12 |
| STAI | 185 | $84.99 |
| CDNS | 1 | $348.69 |
| NVNI | 240 | $139.27 |
| DTCK | 65 | $50.26 |
| MSFT | 0.0255 | $13.34 |

### 📈 Recent trades

- **July 31, 2025 at 2:41:14 PM**: BUY 0.0255 MSFT @ $538.93/share ($13.74)
- **July 31, 2025 at 2:40:29 PM**: SELL 92 RAYA @ $0.1495/share ($13.75)
- **July 30, 2025 at 8:07:05 PM**: BUY 92 RAYA @ $0.1275/share ($11.73)
- **July 30, 2025 at 8:06:32 PM**: SELL 300 TTOO @ $0.0152/share ($4.56)
- **July 30, 2025 at 2:41:08 PM**: BUY 7 IMNN @ $7.16/share ($50.12)
- **July 30, 2025 at 2:40:56 PM**: BUY 300 TTOO @ $0.0152/share ($4.56)
- **July 30, 2025 at 2:40:56 PM**: BUY 11 HLIT @ $9/share ($99.00)
- **July 30, 2025 at 2:40:55 PM**: BUY 65 DTCK @ $0.925/share ($60.13)
- **July 30, 2025 at 2:39:45 PM**: SELL 312 CASK @ $0.7068/share ($220.52)
- **July 30, 2025 at 6:05:33 AM**: BUY 63 ENVB @ $1.23/share ($77.49)

<!-- auto end -->

- [🧠 Logs](./agent.log)
- [🧑‍💻 System prompt](./system-prompt.md)
- [📁 Source code](./agent.ts)

## 🛠️ Installation

1. Clone the repository and reset the agent's thread:

```bash
git clone https://github.com/AnandChowdhary/priced-in.git
cd priced-in
rm thread.json
```

2. Install dependencies:

```bash
npm install
```

3. Set up your OpenAI API key:

```bash
export OPENAI_API_KEY="your-api-key-here"
```

## 🏃‍♂️ Running the agent

The agent's portfolio is stored in `portfolio.json`:

```json
{
  "cash": 95.44,
  "holdings": {
    "AAPL": 4,
    "CLNE": 56
  },
  "history": [
    {
      "date": "2025-06-21T12:43:07.141Z",
      "type": "buy",
      "ticker": "AAPL",
      "shares": 4,
      "price": 201.5,
      "total": 806
    }
  ]
}
```

- **cash**: Available cash balance for trading
- **holdings**: Current stock positions (ticker: number of shares)
- **history**: Complete record of all trades

### Local execution

Run the trading agent manually:

```bash
npm start
```

This will execute one trading session where the agent will:

1. Check the current portfolio
2. Analyze market conditions
3. Make trading decisions
4. Update the portfolio

### Automated execution via GitHub Actions

The agent is configured to run automatically every hour via GitHub Actions. To enable this:

1. Fork this repository
2. Go to Settings → Secrets and variables → Actions
3. Add a new repository secret named `OPENAI_API_KEY` with your OpenAI API key
4. The agent will now run automatically every hour

You can also trigger a manual run from the Actions tab in your GitHub repository.

## ⚠️ Disclaimer

This is an experimental AI trading agent for educational purposes. Real trading involves significant risk. Never invest money you cannot afford to lose.

## 📄 License

[MIT](./LICENSE) © [Anand Chowdhary](https://anandchowdhary.com)
