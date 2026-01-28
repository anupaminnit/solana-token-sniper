# 🎯 Solana Token Sniper

![Solana](https://img.shields.io/badge/Solana-14F195?style=for-the-badge&logo=solana&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

**Detect new Solana token launches instantly and analyze their safety in real-time.**

A powerful, automated tool that monitors the Solana blockchain for new token launches, analyzes their safety metrics, and alerts you to potential opportunities before they go viral.

🔗 **[Live Demo](https://anupaminnit.github.io/solana-token-sniper/)**

---

## 🌟 Features

### 🔍 Auto-Detection
- **Real-time monitoring** of new liquidity pools on Raydium
- **Customizable scan intervals** (10s to 5min)
- **Automatic filtering** by liquidity thresholds
- **Smart deduplication** - never shows the same token twice

### 🛡️ Safety Analysis (0-100 Score)
Every token is automatically analyzed across multiple factors:

| Factor | Points | What It Measures |
|--------|--------|------------------|
| **Liquidity** | 30 | Higher liquidity = lower rug risk |
| **Trade Count** | 20 | More trades = genuine interest |
| **Buy/Sell Ratio** | 25 | Buy pressure vs sell pressure |
| **Launch Age** | 25 | How fresh is the token |

### 🚨 Smart Alerts
- **Color-coded safety ratings** (Excellent → Danger)
- **Positive signals** highlighting strengths
- **Red flags** warning of risks
- **Sound notifications** for high-quality finds
- **Visual indicators** for active monitoring

### ⚡ Quick Actions
Every detected token includes:
- 📋 One-click copy of contract address
- 🔗 Direct link to GMGN analytics
- 🔄 Quick trade on Raydium
- 📊 View live chart on DexScreener

### 📊 Live Dashboard
- **Real-time statistics** of tokens found
- **High-quality counter** for promising tokens
- **Last check timestamp**
- **Countdown to next scan**

---

## 🚀 Quick Start

### Option 1: Use Online (Easiest)
1. Visit the live demo: `https://anupaminnit.github.io/solana-token-sniper/`
2. Enter your BitQuery API key
3. Click "Start Sniping" ▶️
4. Watch new tokens appear automatically!

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/anupaminnit/solana-token-sniper.git

# Navigate to directory
cd solana-token-sniper

# Start local server (Python)
python -m http.server 8000

# Or use Node.js
npx http-server

# Open browser
# Visit: http://localhost:8000
```

---

## 📋 Prerequisites

- **BitQuery API Key** - [Get free key](https://bitquery.io) (required)
- **Web browser** (Chrome, Firefox, Safari, Edge)
- **Internet connection**

---

## 🎮 How to Use

### Step 1: Configure Settings

| Setting | Description | Recommended |
|---------|-------------|-------------|
| **API Key** | Your BitQuery authentication key | Required |
| **Min Liquidity** | Minimum $ in pool to show token | $5,000 - $10,000 |
| **Min Safety Score** | Filter by safety rating | 60+ (Good or better) |
| **Check Interval** | How often to scan | 30 seconds |

### Step 2: Start Sniping
- Click **"▶️ Start Sniping"**
- Monitor the status indicator (🟢 = Active)
- Wait for new tokens to appear

### Step 3: Analyze Results
Each token card shows:
```
┌─────────────────────────────────────────┐
│ TOKEN NAME (SYMBOL)                     │
│ Contract: [clickable address]      XX/100│
├─────────────────────────────────────────┤
│ Liquidity: $X,XXX                       │
│ Trades: XX                              │
│ Buy/Sell: X.XXx                         │
├─────────────────────────────────────────┤
│ ✅ Positives: [badges]                  │
│ ⚠️ Red Flags: [badges]                  │
├─────────────────────────────────────────┤
│ [Trade on Raydium] [View Chart]         │
└─────────────────────────────────────────┘
```

### Step 4: Take Action
- **High Score (80+)**: Strong potential, research immediately
- **Good Score (60-79)**: Worth investigating
- **Medium Score (40-59)**: Proceed with caution
- **Low Score (<40)**: High risk, likely avoid

---

## 📊 Understanding Safety Scores

### 🟢 Excellent (80-100)
- Strong liquidity ($50k+)
- High trade volume
- Strong buy pressure
- Recently launched
- **Action**: Research immediately, potential gem

### 🔵 Good (60-79)
- Good liquidity ($20k+)
- Active trading
- More buyers than sellers
- Fresh launch
- **Action**: Worth investigating

### 🟡 Medium (40-59)
- Moderate liquidity ($10k+)
- Some trading activity
- Mixed buy/sell ratio
- **Action**: Proceed with extreme caution

### 🔴 Low/Danger (0-39)
- Low liquidity
- Few trades
- More selling than buying
- **Action**: Likely avoid, very high risk

---

## ⚙️ Advanced Configuration

### Customizing Filters

**For Conservative Sniping:**
```
Min Liquidity: $50,000
Min Safety Score: 80
Check Interval: 1 minute
```

**For Aggressive Sniping:**
```
Min Liquidity: $1,000
Min Safety Score: 40
Check Interval: 10 seconds
```

**Balanced Approach (Recommended):**
```
Min Liquidity: $5,000
Min Safety Score: 60
Check Interval: 30 seconds
```

---

## 🛡️ Safety & Security

### ⚠️ Important Disclaimers

- ❌ **This is NOT financial advice**
- ❌ **High returns = High risk**
- ❌ **Always do your own research (DYOR)**
- ❌ **Never invest more than you can afford to lose**
- ❌ **Many new tokens are scams or rug pulls**

### 🔒 Security Features

- ✅ API key stored **locally in browser only**
- ✅ No data sent to third-party servers
- ✅ All queries direct to BitQuery & Solana RPC
- ✅ Open source - inspect the code yourself

### 🚩 Red Flags to Watch For

Even with a good score, be cautious of:
- 🚩 No social media presence
- 🚩 Anonymous dev team
- 🚩 Unrealistic promises
- 🚩 Locked liquidity less than 1 year
- 🚩 High dev wallet holdings
- 🚩 Contract not verified

---

## 🔧 Technical Details

### Built With
- **Frontend**: HTML5, JavaScript (Vanilla)
- **Styling**: TailwindCSS
- **Data Source**: BitQuery GraphQL API
- **Blockchain**: Solana (Raydium DEX)

### How It Works

1. **Polling**: Queries BitQuery every X seconds
2. **Filtering**: Applies liquidity and time filters
3. **Analysis**: Calculates safety score based on metrics
4. **Display**: Shows tokens meeting your criteria
5. **Tracking**: Prevents duplicate displays

### API Rate Limits
- BitQuery Free Tier: ~10-20 requests/min
- Recommended interval: 30 seconds or more
- Consider paid plan for faster scanning

---

## 📚 Use Cases

### 🎯 Early Token Discovery
Find tokens within minutes of launch before they're discovered by the masses.

### 💎 Gem Hunting
Filter for high-quality tokens with strong fundamentals and early momentum.

### 🔍 Market Research
Study patterns in new token launches and trading behavior.

### 📊 Portfolio Building
Discover potential investment opportunities in real-time.

---

## 🐛 Troubleshooting

### Tokens Not Appearing
- ✅ Check API key is entered correctly
- ✅ Verify BitQuery subscription is active
- ✅ Lower minimum liquidity threshold
- ✅ Lower minimum safety score
- ✅ Check browser console for errors

### "Failed to fetch" Error
- ✅ Check internet connection
- ✅ Verify API key is valid
- ✅ Run on local server (not file://)
- ✅ Check if BitQuery API is operational

### False Positives
- The tool shows opportunities, but **you must verify**
- Always check: contract, liquidity lock, dev holdings
- Use additional tools: RugCheck, BubbleMaps

---

## 🚀 Roadmap

### Planned Features
- [ ] Telegram/Discord bot integration
- [ ] Historical tracking of found tokens
- [ ] Performance analytics (ROI tracking)
- [ ] Wallet monitoring (track specific addresses)
- [ ] Auto-buy functionality (advanced)
- [ ] Multi-DEX support (Orca, Meteora)
- [ ] Contract verification checking
- [ ] Social sentiment analysis
- [ ] Export to CSV/Excel

### Community Requests
Open an issue to suggest features!

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 💬 Support

- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/anupaminnit/solana-token-sniper/issues)
- 💡 **Feature Requests**: [GitHub Discussions](https://github.com/anupaminnit/solana-token-sniper/discussions)
- 📧 **Email**: anupamsd2403@outlook.com

---

## ⚠️ Disclaimer

**This tool is for educational and research purposes only.**

- Cryptocurrency trading carries substantial risk
- Past performance does not indicate future results
- The developers are not liable for any financial losses
- Always verify information from multiple sources
- Only invest what you can afford to lose
- Consult a financial advisor before making investment decisions

**Use at your own risk. Trading cryptocurrencies can result in the loss of your entire investment.**

---

## 🙏 Acknowledgments

- **BitQuery** - For excellent blockchain data API
- **Solana** - For the fast, scalable blockchain
- **Raydium** - For DEX infrastructure
- **The Community** - For feedback and support

---

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/anupaminnit/solana-token-sniper?style=social)
![GitHub forks](https://img.shields.io/github/forks/anupaminnit/solana-token-sniper?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/anupaminnit/solana-token-sniper?style=social)

---

**⭐ Star this repo if you find it useful!**

**Made with ❤️ by [Anupam](https://github.com/anupaminnit) for the Solana community**

---

## 🔗 Related Projects

- [Solana Wallet Tracker](https://github.com/anupaminnit/solana-wallet-tracker) - Track diamond hands who hold
- More coming soon...

---

*Last Updated: January 2026*
