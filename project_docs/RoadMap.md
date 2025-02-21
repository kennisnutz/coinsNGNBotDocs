
---

# **CoinsNGNBot Version History and Roadmap**

## **v0.0 Series: Foundational Development**

### **v0.0.01** (Initial Release)
- **Description**: The initial version of the bot. Implements the `/price` command to fetch the latest USD exchange rate directly from the CBN website.
- **Features**:
	- Scrapes the CBN website for USD exchange rate data in real time.
	- Responds to user requests for the latest exchange rate via Telegram.
- **Limitations**:
	- Slow response time due to live scraping (~8–15 seconds).
	- Only supports USD exchange rate queries.

---

### **v0.0.02** (Performance Optimization)
- **Description**: Optimizes response time by introducing a data store and periodic background updates for the USD exchange rate.
- **Features**:
	- Implements a data store to maintain the latest USD exchange rate and its timestamp.
	- Adds a background process that fetches the USD exchange rate from the CBN website at 30-second intervals.
	- Improves user experience by instantly retrieving exchange rate data from the local data store during requests.
	- Provides more precise pricing data ie sell price and buy price as qouted by CBN website
- **Benefits**:
	- Drastically reduced response time (near-instantaneous).
	- Decreased dependency on real-time network requests during user interactions.

---

### **v0.0.03** (Multi-Currency Support)
- **Description**: Expands functionality to support additional currencies: CAD, EUR, and GBP.
- **Features**:
	- Adds data stores for CAD, EUR, and GBP exchange rates.
	- Updates the background process to fetch and store exchange rates for all supported currencies.
	- Extends Telegram handlers to process commands like `/price CAD`, `/price EUR`, and `/price GBP`.
- **Benefits**:
	- Supports user queries for multiple fiat currencies.
	- Scales the bot’s functionality to address broader use cases.

---

### **v0.0.04** (Cryptocurrency Support)
- **Description**: Introduces support for the top 10 cryptocurrencies' exchange rates.
- **Features**:
	- Creates data stores for exchange rates of Bitcoin (BTC), Ethereum (ETH), Binance Coin (BNB), and other leading cryptocurrencies.
	- Adds background tasks to update cryptocurrency exchange rates periodically via a reliable API (e.g., CoinGecko or CoinMarketCap).
	- Implements Telegram handlers for commands like `/price BTC`, `/price ETH`, etc.
- **Benefits**:
	- Enables users to query both fiat and cryptocurrency exchange rates.
	- Positions the bot as a versatile tool for both traditional and crypto traders.

---

### **v0.0.05** (Commodity Support)
- **Description**: Adds support for commodity prices such as Gold, Silver, Lithium, Iron, Oil, and Cocoa.
- **Features**:
	- Establishes data stores for commodity prices.
	- Integrates with an external API for periodic updates on commodity prices.
	- Adds commands like `/price Gold`, `/price Oil`, and `/price Cocoa` to the bot.
- **Benefits**:
	- Expands the bot’s utility to include commodities, appealing to a wider audience.
	- Completes the **v0.0 series**, setting the foundation for more advanced features.

---

## **Future Plans: v0.1 Series**
The **v0.1 series** will focus on enhancing user interaction, improving UI/UX, and integrating advanced analytics and customization options. Possible features include:
1. **v0.1.01**: Custom notifications for exchange rate thresholds.
2. **v0.1.02**: Historical data queries and trend analysis.
3. **v0.1.03**: Support for localized currencies and languages.
4. **v0.1.04**: Admin dashboard for bot configuration and monitoring.
5. **v0.1.05**: Advanced analytics and insights for traders.

---

## **Version Documentation and Maintenance**
- Each version will have detailed documentation, including:
	1. **Version Name** and **Release Date**.
	2. **Scope of Changes** (features added, bugs fixed, and optimizations made).
	3. **Known Issues** or limitations (if any).
	4. **Performance Metrics** before and after updates (e.g., response time improvement).

---
