# 🚀 Solana PumpFun Sniper Bot | Liquidity Sniper | Auto Trading Bot  

Welcome to the **Solana PumpFun Sniper Bot** – a high-performance trading bot designed to identify and execute trades on new liquidity pools on the Solana blockchain. With lightning-fast execution and built-in safety checks, the bot empowers traders to take advantage of newly launched tokens on **PumpFun** and other decentralized exchanges (DEXs).  

> **Disclaimer**: This bot is provided for educational and experimental purposes only. Use at your own risk.  

---

## 🔥 Key Features  

- **⚡ Rapid USDC/WSOL Sniping**  
   Automatically detects and purchases tokens from new liquidity pools before they appear in the PumpFun UI.  
- **📊 Automated Trading**  
   Execute trades with configurable take-profit and stop-loss settings.  
- **💧 Liquidity Protection**  
   Perform minimum liquidity checks to avoid low-volume pools.  
- **🔒 Token Safety Verifications**  
   - Burn/Lock liquidity checks.  
   - Ownership renounce checks to minimize rug-pull risk.  
- **🚀 High-Speed Performance**  
   Built for speed, the bot leverages WebSocket connections and optimized RPC nodes for near-instant execution.  

---

## 💡 What Can You Use It For?  

This bot is perfect for:  
- **Solana Token Sniping**: Be the first to buy tokens from new pools.  
- **PumpFun Trading**: Automate your buy and sell orders for new token pairs.  
- **Liquidity Sniping**: Detect and act on new liquidity events in real-time.  
- **Auto Profit/Loss Execution**: Manage risk with take-profit and stop-loss settings.  
- **Whitelist Trading**: Target specific tokens by maintaining a snipe list.  

---

## 📦 How to Get Started  

### **1. Prerequisites**  

Before running the bot, ensure you have the following:  
- A **Solana wallet** (e.g., Phantom, Sollet).  
- Sufficient **SOL** to cover transactions.  
- Swap some **SOL** for **USDC** or **WSOL**, depending on your configuration. (Use tools like [Jupiter](https://jup.ag/)).  
- An RPC provider like **Shyft**, **Helius**, or **QuickNode** for reliable connections.  

### **2. Setup Steps**  

1. **Clone the Repository**  
   ```bash  
   git clone https://github.com/bitfancy/pumpfun-sniper-bot.git  
   cd pumpfun-sniper-bot  
   ```  

2. **Install Dependencies**  
   ```bash  
   npm install  
   ```  

3. **Configure the Environment**  
   - Rename the `.env.copy` file to `.env`.  
   - Edit the file to include your wallet’s private key, RPC endpoints, and bot settings.  

4. **Run the Bot**  
   Start the bot by executing the following command:  
   ```bash  
   npm run buy  
   ```  

---

## ⚙️ Configuration  

Here’s an overview of the key settings available in the `.env` file:  

| **Parameter**              | **Description**                                                                                       |  
|----------------------------|-------------------------------------------------------------------------------------------------------|  
| `PRIVATE_KEY`              | Your wallet’s private key (required for signing transactions).                                        |  
| `RPC_ENDPOINT`             | The HTTP RPC endpoint for interacting with the Solana blockchain.                                     |  
| `RPC_WEBSOCKET_ENDPOINT`   | The WebSocket RPC endpoint for real-time event tracking.                                              |  
| `QUOTE_MINT`               | The base currency for sniping (choose **USDC** or **WSOL**).                                          |  
| `QUOTE_AMOUNT`             | The amount of USDC/WSOL to use per trade.                                                             |  
| `CHECK_IF_IS_BURNED`       | Enable/disable liquidity burn checks.                                                                 |  
| `CHECK_IF_IS_LOCKED`       | Enable/disable liquidity lock checks.                                                                 |  
| `MIN_POOL_SIZE`            | Minimum liquidity required to execute trades.                                                        |  
| `TAKE_PROFIT`              | Take-profit percentage (default: 200%).                                                              |  
| `STOP_LOSS`                | Stop-loss percentage (default: 50%).                                                                 |  
| `USE_SNIPE_LIST`           | Restrict sniping to tokens in a whitelist (requires `snipe-list.txt`).                                |  
| `SNIPE_LIST_REFRESH_INTERVAL` | Interval (in milliseconds) to refresh the snipe list.                                              |  
| `AUTO_SELL`                | Automatically sell tokens after purchase (set to `true` or `false`).                                 |  

---

## ✨ Advanced Features  

### **1. Take-Profit/Stop-Loss**  
Configure the bot to automatically sell tokens based on price movements:  
- Set **TAKE_PROFIT** (e.g., 200% to sell when token price doubles).  
- Set **STOP_LOSS** (e.g., 50% to sell if price drops below 50%).  

### **2. Whitelist Sniping (Snipe List)**  
Only trade specific tokens by enabling `USE_SNIPE_LIST` and listing token mint addresses in `snipe-list.txt`.  

### **3. Auto-Sell Behavior**  
- **Enable Auto-Sell**: Tokens will automatically sell after reaching profit targets or time delays.  
- **Custom Delay**: Adjust `AUTO_SELL_DELAY` for a timed sell after purchase.  

### **4. Token Safety Checks**  
- Avoid scam tokens with **Burn/Lock** and **Ownership Renounce** checks.  
- Protect funds by only trading tokens that meet liquidity requirements (`MIN_POOL_SIZE`).  

---

## 🔧 Troubleshooting  

### **Common Issues and Fixes**  

| **Issue**                   | **Fix**                                                                                     |  
|-----------------------------|---------------------------------------------------------------------------------------------|  
| Empty transactions on SolScan | Set `COMMITMENT_LEVEL` to `finalized`.                                                    |  
| Unsupported RPC node         | Switch to a more compatible RPC provider (e.g., Shyft, Helius, QuickNode).                 |  
| Missing token account        | Ensure your wallet has sufficient USDC/WSOL before running the bot.                        |  

If you encounter other issues, set `LOG_LEVEL=debug` in `.env` and report them on the repository.  

---

## 📜 Disclaimer  

This bot is intended for educational purposes only. The developer is not liable for any losses incurred while using the bot. Always use caution and test with small amounts before committing significant funds.  

---

## 📞 Contact  

Need help? Feel free to reach out!  

- **Telegram**: [@bitfancy](https://t.me/bitfancy)  
- **GitHub Repository**: [PumpFun Sniper Bot](https://github.com/bitfancy/pumpfun-sniper-bot)  

---

## 🌟 Contribute  

Contributions are welcome! If you have suggestions or improvements, please open a pull request or create an issue in the repository.  

---

Start leveraging the **Solana PumpFun Sniper Bot** today to maximize your trading efficiency!  
