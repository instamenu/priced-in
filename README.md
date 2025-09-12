# 🤖 Priced In

An autonomous AI-powered stock trading agent that executes trades on GitHub Actions, built with OpenAI's Agents framework.

<!-- auto start -->

## 💰 Portfolio value: $903.97** (-61.95% CAGR)

### 📊 Holdings

| Asset | Shares | Value |
|-------|--------|-------|
| Cash | - | $1.20 |
| HLIT | 11 | $108.90 |
| STAI | 185 | $80.46 |
| CDNS | 1 | $347.37 |
| NVNI | 240 | $146.52 |
| MSFT | 0.0255 | $12.92 |
| AMBA | 1 | $82.24 |
| LMND | 1 | $50.96 |
| CCLD | 11 | $42.79 |
| LTRY | 14 | $19.18 |
| PRSO | 9 | $11.43 |

### 📈 Recent trades

- **September 11, 2025 at 2:46:07 PM**: BUY 9 PRSO @ $1.31/share ($11.79)
- **September 11, 2025 at 2:41:24 PM**: SELL 19 UGRO @ $0.62/share ($11.78)
- **September 9, 2025 at 2:45:47 PM**: BUY 14 LTRY @ $1.37/share ($19.18)
- **September 9, 2025 at 2:42:16 PM**: SELL 10 WOLF @ $1.755/share ($17.55)
- **September 8, 2025 at 2:45:19 PM**: BUY 11 CCLD @ $3.41/share ($37.51)
- **September 8, 2025 at 2:41:35 PM**: SELL 7 IMNN @ $5.74/share ($40.18)
- **September 4, 2025 at 8:12:14 PM**: BUY 19 UGRO @ $0.5137/share ($9.76)
- **September 4, 2025 at 8:10:19 PM**: SELL 14 KLTO @ $0.69/share ($9.66)
- **September 3, 2025 at 2:43:31 PM**: BUY 14 KLTO @ $0.6161/share ($8.63)
- **September 3, 2025 at 2:41:47 PM**: BUY 1 LMND @ $51.88/share ($51.88)

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
