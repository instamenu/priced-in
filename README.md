# 🤖 Priced In

An autonomous AI-powered stock trading agent that executes trades on GitHub Actions, built with OpenAI's Agents framework.

<!-- auto start -->

## 💰 Portfolio value: $882.34** (-72.20% CAGR)

### 📊 Holdings

| Asset | Shares | Value |
|-------|--------|-------|
| Cash | - | $0.27 |
| HLIT | 11 | $105.05 |
| IMNN | 7 | $49.00 |
| STAI | 185 | $71.47 |
| CDNS | 1 | $343.81 |
| NVNI | 240 | $146.40 |
| MSFT | 0.0255 | $12.89 |
| WOLF | 10 | $13.45 |
| AMBA | 1 | $79.68 |
| LMND | 1 | $51.69 |
| KLTO | 14 | $8.63 |

### 📈 Recent trades

- **September 3, 2025 at 2:43:31 PM**: BUY 14 KLTO @ $0.6161/share ($8.63)
- **September 3, 2025 at 2:41:47 PM**: BUY 1 LMND @ $51.88/share ($51.88)
- **September 3, 2025 at 2:39:00 PM**: SELL 65 DTCK @ $0.9298/share ($60.44)
- **August 26, 2025 at 2:41:34 PM**: BUY 1 AMBA @ $72/share ($72.00)
- **August 26, 2025 at 2:41:34 PM**: BUY 10 WOLF @ $1.335/share ($13.35)
- **August 26, 2025 at 2:38:29 PM**: SELL 63 ENVB @ $1.36/share ($85.68)
- **July 31, 2025 at 2:41:14 PM**: BUY 0.0255 MSFT @ $538.93/share ($13.74)
- **July 31, 2025 at 2:40:29 PM**: SELL 92 RAYA @ $0.1495/share ($13.75)
- **July 30, 2025 at 8:07:05 PM**: BUY 92 RAYA @ $0.1275/share ($11.73)
- **July 30, 2025 at 8:06:32 PM**: SELL 300 TTOO @ $0.0152/share ($4.56)

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
