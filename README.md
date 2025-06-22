# Advanced Cryptocurrency Trading System

Professional-grade crypto trading system leveraging CoinGecko's free API. Features multi-asset support, technical indicators, backtesting framework, and performance analytics with robust rate limit handling.
This is more like an enhanced cryptocurrency trading system with these key upgrades from the original Yahoo Finance-based version which can be found in this github repository: https://github.com/johnnietse/cryptocurrency-trading-system.git

## 🔑 Key Features
- **Multi-Asset and Currency Support**: The system analyzes 15+ major cryptocurrencies (BTC, ETH, SOL, etc.) and up to 62+ currencies are supported by CoinGecko API
- **CoinGecko API Integration**: Free tier access with intelligent rate limit management (can be upgraded to a CoinGecko API with full subscription)
- **Technical Indicators**: Dual moving averages (10-day/40-day) for signal generation
- **Backtesting Engine**: Simulate strategy vs buy-and-hold performance
- **Advanced Visualizations**: Professional trading charts and comparisons
- **Risk Metrics**: Sharpe ratio, volatility, drawdown, and MSE calculations

## ⚙️ Installation
```bash
git clone https://github.com/johnnietse/cryptocurrency-trading-system-with-coingecko-api.git
cd cryptocurrency-trading-system-with-coingecko-api
```

## Requirements
```bash
pandas numpy matplotlib seaborn scikit-learn
```

## Usage
- Configure assets and capital:
```python
# advanced_crypto_trading_system_api.py
ASSETS = ['BTC-USD', 'ETH-USD', 'SOL-USD']  # Add/remove assets
INITIAL_CAPITAL = 10000.0                   # Starting portfolio value
```

- Run the main script:
```bash
python Advanced_Crypto_Trading_System_with_Coingecko_API.py
```

## Sample Output
```text
======================================================================
FREE CRYPTO TRADING SYSTEM
Powered by CoinGecko Free API
Enhanced with Robust Rate Limit Handling
======================================================================
Assets: BTC-USD, ETH-USD, LTC-USD, XRP-USD, ADA-USD, DOGE-USD, SOL-USD, BNB-USD, DOT-USD, AVAX-USD, MATIC-USD, SHIB-USD, TRX-USD, LINK-USD, ATOM-USD
Date Range: 2024-06-21 to 2025-06-21
Initial Capital: $10,000.00
Using CoinGecko Free Tier API (no key required)

Visualizations will be saved to: /content/trading_visualizations
Fetching market data from CoinGecko API...
Starting data fetch for 15 assets...
[1/15] Fetching BTC-USD (bitcoin)...
Rate control: Waiting 15.0s
Successfully fetched BTC-USD data (366 records)
[2/15] Fetching ETH-USD (ethereum)...
Rate control: Waiting 14.9s
Successfully fetched ETH-USD data (366 records)
[3/15] Fetching LTC-USD (litecoin)...
Rate control: Waiting 15.0s
Successfully fetched LTC-USD data (366 records)
[4/15] Fetching XRP-USD (ripple)...
Rate control: Waiting 15.0s
Successfully fetched XRP-USD data (366 records)
[5/15] Fetching ADA-USD (cardano)...
Rate control: Waiting 15.0s
Successfully fetched ADA-USD data (366 records)
[6/15] Fetching DOGE-USD (dogecoin)...
Rate control: Waiting 15.0s
Successfully fetched DOGE-USD data (366 records)
[7/15] Fetching SOL-USD (solana)...
Rate control: Waiting 15.0s
Successfully fetched SOL-USD data (366 records)
[8/15] Fetching BNB-USD (binancecoin)...
Rate control: Waiting 15.0s
Successfully fetched BNB-USD data (366 records)
[9/15] Fetching DOT-USD (polkadot)...
Rate control: Waiting 15.0s
Successfully fetched DOT-USD data (366 records)
[10/15] Fetching AVAX-USD (avalanche-2)...
Rate control: Waiting 15.0s
Successfully fetched AVAX-USD data (366 records)
[11/15] Fetching MATIC-USD (matic-network)...
Rate control: Waiting 15.0s
Successfully fetched MATIC-USD data (366 records)
[12/15] Fetching SHIB-USD (shiba-inu)...
Rate control: Waiting 14.9s
Successfully fetched SHIB-USD data (366 records)
[13/15] Fetching TRX-USD (tron)...
Rate control: Waiting 15.0s
Successfully fetched TRX-USD data (366 records)
[14/15] Fetching LINK-USD (chainlink)...
Rate control: Waiting 15.0s
Successfully fetched LINK-USD data (366 records)
[15/15] Fetching ATOM-USD (cosmos)...
Rate control: Waiting 15.0s
Successfully fetched ATOM-USD data (366 records)

API Usage Report:
Total API Calls: 15
Time Elapsed: 227.77 seconds
Requests per minute: 3.95

Data retrieval complete in 227.77 seconds

======================================================================
ANALYZING: BTC-USD
======================================================================
Data range: 2024-06-21 to 2025-06-21
Records: 366
First Close: $64,844.67
Last Close: $103,290.11
Price Change: 59.29%

Strategy Signals:
Buy Signals: 4, Sell Signals: 4

Backtest Results:
Final Strategy Value: $14,945.18 (Profit: $4,945.18)
Final Buy & Hold Value: $15,928.85 (Profit: $5,928.85)

Performance Metrics:
Total Return: 49.45%
Annual Volatility: 27.79%
Sharpe Ratio: 1.13
Max Drawdown: -22.54%
MSE vs Buy&Hold: 2,083,701.56
Saved signal plot: trading_visualizations/BTC-USD_signals_20250621_000411.png
Saved performance plot: trading_visualizations/BTC-USD_performance_20250621_000411.png
```



## Rate Limit Management
System features intelligent API management:
- Automatic 15-second delays between requests
- Exponential backoff during rate limit errors (5s → 10s → 20s)
- Usage tracking:
```text
API Usage Report:
Total API Calls: 15
Time Elapsed: 227.77 seconds
Requests per minute: 3.95
```

## Notebook/Script Structure

```text
CryptoDataFetcher/         # Market data acquisition
├── fetch_market_data()    # API requests + rate limits
└── coin_ids dictionary    # 28+ imported cryptocurrencies

TradingSignalsGenerator/   # Technical analysis
├── compute_moving_averages()
└── generate_trading_signals()

PortfolioSimulator/        # Backtesting engine
└── simulate_strategy()    # Returns + comparisons

TradingVisualizer/         # Visualization tools
├── plot_price_signals()
└── plot_performance_comparison()
```


## Examples

### ADA-USD
![ADA-USD_performance_20250620_201710](https://github.com/user-attachments/assets/d4e8638d-f26d-45fc-b1f7-4a6cad35151d)
![ADA-USD_signals_20250620_201710](https://github.com/user-attachments/assets/2898edb3-23e3-4c09-8bad-aca69e011f16)

### ATOM-USD
![ATOM-USD_performance_20250620_201719](https://github.com/user-attachments/assets/3787ddb5-2b2f-451a-94d2-f547fd0f8c07)
![ATOM-USD_signals_20250620_201718](https://github.com/user-attachments/assets/bb81643a-1dc7-4ba9-8edc-d33c78955f8f)

### AVAX-USD
![AVAX-USD_performance_20250620_201714](https://github.com/user-attachments/assets/c8299a7e-01be-4744-8e5e-e65a1aee4132)
![AVAX-USD_signals_20250620_201714](https://github.com/user-attachments/assets/a179df55-3d2c-40a0-8849-16be23e63ca3)

### BNB-USD
![BNB-USD_performance_20250620_201713](https://github.com/user-attachments/assets/bf386dac-a429-4dd5-a228-c3f1cc9bb861)
![BNB-USD_signals_20250620_201712](https://github.com/user-attachments/assets/92d23a11-3b9c-4c7c-8f80-3d64a94cd0d3)

### BTC-USD
![BTC-USD_performance_20250620_201706](https://github.com/user-attachments/assets/c1920d8e-51a3-40a8-b1ef-cd9c79a2eadd)
![BTC-USD_signals_20250620_201212](https://github.com/user-attachments/assets/ad07f098-de32-4e1d-b4a9-07f627396229)
![BTC-USD_signals_20250620_201706](https://github.com/user-attachments/assets/e2b7a513-a810-4f09-94d8-ebef2784dac6)

### DOT-USD
![DOT-USD_performance_20250620_201714](https://github.com/user-attachments/assets/6e017e23-2c62-4978-8dd0-ae77006d7350)
![DOT-USD_signals_20250620_201713](https://github.com/user-attachments/assets/754b4d60-d24c-4ee6-ae74-8add32b5ac85)

### DOGE-USD
![DOGE-USD_performance_20250620_201711](https://github.com/user-attachments/assets/3a2c7d20-68e2-4eda-b594-521d462eea3e)
![DOGE-USD_signals_20250620_201711](https://github.com/user-attachments/assets/fac36e54-ccae-441b-8ba0-9a91e0297b1c)

### ETH-USD
![ETH-USD_performance_20250620_201708](https://github.com/user-attachments/assets/a8411f9b-84f6-41c5-99ad-b4d60e0a74a7)
![ETH-USD_signals_20250620_201707](https://github.com/user-attachments/assets/5dc3b21a-acea-456e-8f63-c1d905b1158d)

### LINK-USD
![LINK-USD_performance_20250620_201718](https://github.com/user-attachments/assets/5d140bd8-ab4d-4cf3-94a5-ccbeba2b3390)
![LINK-USD_signals_20250620_201717](https://github.com/user-attachments/assets/1ab5a39c-15ac-49fc-8383-09792ab2786a)

### LTC-USD
![LTC-USD_performance_20250620_201709](https://github.com/user-attachments/assets/83a514a9-7354-44ce-b0e2-b7617427aea3)
![LTC-USD_signals_20250620_201708](https://github.com/user-attachments/assets/256c6c50-0a8c-4205-9538-a6e7e73ca709)

### MATIC-USD
![MATIC-USD_performance_20250620_201715](https://github.com/user-attachments/assets/2a39efb9-ae37-4d4c-942b-99874cd9f64c)
![MATIC-USD_signals_20250620_201715](https://github.com/user-attachments/assets/e6f74542-2550-4a03-9fe3-24a058ad0336)

### SHIB-USD
![SHIB-USD_performance_20250620_201716](https://github.com/user-attachments/assets/d2040c83-d2c6-4254-8a0a-d56dc1558d95)
![SHIB-USD_signals_20250620_201716](https://github.com/user-attachments/assets/b81f597d-0514-4b10-95c6-45be2c8d8f91)

### SOL-USD
![SOL-USD_performance_20250620_201712](https://github.com/user-attachments/assets/18de576d-801d-4ad0-aec7-05d681cc6991)
![SOL-USD_signals_20250620_201712](https://github.com/user-attachments/assets/a17c9d84-a6cc-4f70-ba39-bcfd46b2d16d)

### TRX-USD
![TRX-USD_performance_20250620_201717](https://github.com/user-attachments/assets/39bf4959-1446-4281-867b-aa99a965bc66)
![TRX-USD_signals_20250620_201717](https://github.com/user-attachments/assets/238dbe0d-e2ef-444f-8630-fb5eee91e2ec)

### XRP-USD
![XRP-USD_performance_20250620_201709](https://github.com/user-attachments/assets/d18b590a-7afe-488f-a214-211a8ddf14fa)
![XRP-USD_signals_20250620_201709](https://github.com/user-attachments/assets/6f722af6-47ef-4061-b671-523cb656edf0)


## Updates in Version 2 (Advanced_Cryptocurrency_Trading_System_API_V2.py and Advanced_Cryptocurrency_Trading_System_API_V2.ipynb)
### Core Improvements:
1. Enhanced Rate Limit Handling:
- Added header-based rate limit detection (x-ratelimit-remaining)
- Implemented smarter cooldown logic with 60s wait when near limit
- Added practical troubleshooting advice for failed fetches

2. More Realistic Trading Simulation:
- Introduced 0.1% trading fees per transaction
- Added volatility-based position sizing (reduces exposure during high volatility)
- Switched to Exponential Moving Averages (EMA) instead of SMA

3. Performance Optimizations:
- Replaced class-based structure with functional approach
- Reduced asset coverage from 29 to 15 coins
- Shortened backtest period from 1 year to 6 months
- Simplified metrics calculation (removed MSE vs Buy & Hold)

4. Data Processing Improvements:
- Better handling of empty price data responses
- Added minimum data threshold (10 records) for analysis
- Improved OHLC resampling logic

### Visualization Updates:
- More compact chart sizing (12x6 inches)
- Cleaner annotation styling with white-background boxes
- Unified timestamp format in filenames
- Removed seaborn dependency (uses ggplot style only)

### Bug Fixes:
- Fixed look-ahead bias in strategy returns calculation (shift(1))
- Added proper handling of empty datasets
- Solved timestamp alignment issues in resampling
- Added PerformanceWarning suppression

### Other Changes:
- Initial capital reduced from $10,000 to $5,000
- Output directory renamed to crypto_trading_results
- More detailed console output with progress indicators
- Removed external dependencies (seaborn, scikit-learn)


## Why Version 2 is More Practical for Real-World Trading
1. 💰 Realistic Trading Costs
- Added 0.1% transaction fees per trade
- Accounts for slippage and broker commissions
- Mirrors actual trading expenses ignored in V1

2. 📉 Risk-Managed Position Sizing
- Volatility-based sizing reduces exposure during high volatility
- Prevents overexposure during market turbulence
- Simulates professional risk management practices

3. ⏱️ Avoids Look-Ahead Bias
- Fixed critical error: shift(1) prevents using same-day signals
- Eliminates unrealistic forward-testing advantage
- Matches real trading execution constraints

4. 🔍 Focused Asset Selection
- Reduced from 29 to 15 major coins
- Removes low-liquidity assets (like FLOW, VET, ICP)
- Concentrates on tradable coins with sufficient volume

5. 🚦 Enhanced API Reliability
- Header-based rate limit detection (x-ratelimit-remaining)
- 60-second cool-down when near API limits
- Practical error recovery guidance for users

6. ⚖️ More Relevant Timeframe
- 6-month backtest period (vs 1-year in V1)
- Better reflects current market conditions
- More responsive to recent volatility patterns

7. 📈 Improved Technical Strategy
- Switched to Exponential Moving Averages (EMA)
- More responsive to price changes than SMA
- Standard professional tool (MACD component)

8. 🧮 Realistic Capital Allocation
- $5,000 starting capital (vs $10,000)
- More accessible for retail traders
- Better matches typical account sizes

9. ⚡ Performance Optimizations
- Functional programming approach
- Faster execution with large datasets
- 60%+ reduction in runtime

10. 🛡️ Robust Error Handling
- Minimum 10-record threshold for analysis
- Skip assets with insufficient data
- Prevents false positives from low-quality data

Overall, Version 2 delivers more actionable results because:
- The 6-month test period reflects current market dynamics
- Transaction costs make profitability thresholds realistic
- Volatility-adjusted sizing prevents catastrophic losses
- EMA signals react faster to crypto market volatility
- Focused assets avoid untradable "ghost coins"


## Sample Output
```text
==================================================
PRACTICAL CRYPTO TRADING ANALYZER
Date Range: 2024-12-24 to 2025-06-22
==================================================

Fetching data for 15 coins...
  1/15: BTC-USD...Checkmark! 181 days
  2/15: ETH-USD...Checkmark! 181 days
  3/15: LTC-USD...Checkmark! 181 days
  4/15: XRP-USD...Checkmark! 181 days
  5/15: ADA-USD...Checkmark! 181 days
  6/15: DOGE-USD...Checkmark! 181 days
  7/15: SOL-USD...Checkmark! 181 days
  8/15: BNB-USD...Checkmark! 181 days
  9/15: DOT-USD...Checkmark! 181 days
  10/15: AVAX-USD...Checkmark! 181 days
  11/15: MATIC-USD...Checkmark! 181 days
  12/15: SHIB-USD...Checkmark! 181 days
  13/15: TRX-USD...Checkmark! 181 days
  14/15: LINK-USD...Checkmark! 181 days
  15/15: ATOM-USD...Checkmark! 181 days

===== Analyzing BTC-USD =====
Records: 181
First: $94,644.91 | Last: $101,532.57 | Change: 7.3%
Strategy Final: $5,131.76
Buy & Hold Final: $5,363.87
Total Return: 2.6%
Buy&Hold Return: 7.3%
Volatility: 19.5%
B&H Volatility: 39.4%
Max Drawdown: 10.6%
Saved charts to crypto_trading_results/

===== Analyzing ETH-USD =====
Records: 181
First: $3,414.64 | Last: $2,270.58 | Change: -33.5%
Strategy Final: $5,111.17
Buy & Hold Final: $3,324.77
Total Return: 2.2%
Buy&Hold Return: -33.5%
Volatility: 29.4%
B&H Volatility: 67.1%
Max Drawdown: 13.2%
Saved charts to crypto_trading_results/

===== Analyzing LTC-USD =====
Records: 181
First: $106.30 | Last: $79.71 | Change: -25.0%
Strategy Final: $4,059.83
Buy & Hold Final: $3,749.33
Total Return: -18.8%
Buy&Hold Return: -25.0%
Volatility: 29.0%
B&H Volatility: 68.7%
Max Drawdown: 22.1%
Saved charts to crypto_trading_results/

===== Analyzing XRP-USD =====
Records: 181
First: $2.25 | Last: $2.04 | Change: -9.3%
Strategy Final: $4,392.34
Buy & Hold Final: $4,533.23
Total Return: -12.1%
Buy&Hold Return: -9.3%
Volatility: 26.5%
B&H Volatility: 80.4%
Max Drawdown: 19.4%
Saved charts to crypto_trading_results/

===== Analyzing ADA-USD =====
Records: 181
First: $0.92 | Last: $0.55 | Change: -40.3%
Strategy Final: $3,837.07
Buy & Hold Final: $2,983.66
Total Return: -23.3%
Buy&Hold Return: -40.3%
Volatility: 23.3%
B&H Volatility: 114.7%
Max Drawdown: 25.9%
Saved charts to crypto_trading_results/

===== Analyzing DOGE-USD =====
Records: 181
First: $0.32 | Last: $0.15 | Change: -52.7%
Strategy Final: $5,186.49
Buy & Hold Final: $2,366.72
Total Return: 3.7%
Buy&Hold Return: -52.7%
Volatility: 31.3%
B&H Volatility: 81.5%
Max Drawdown: 15.1%
Saved charts to crypto_trading_results/

===== Analyzing SOL-USD =====
Records: 181
First: $189.84 | Last: $133.71 | Change: -29.6%
Strategy Final: $5,504.54
Buy & Hold Final: $3,521.61
Total Return: 10.1%
Buy&Hold Return: -29.6%
Volatility: 29.6%
B&H Volatility: 78.6%
Max Drawdown: 11.8%
Saved charts to crypto_trading_results/

===== Analyzing BNB-USD =====
Records: 181
First: $692.29 | Last: $626.57 | Change: -9.5%
Strategy Final: $4,511.28
Buy & Hold Final: $4,525.36
Total Return: -9.8%
Buy&Hold Return: -9.5%
Volatility: 18.8%
B&H Volatility: 38.5%
Max Drawdown: 21.0%
Saved charts to crypto_trading_results/

===== Analyzing DOT-USD =====
Records: 181
First: $7.36 | Last: $3.30 | Change: -55.2%
Strategy Final: $4,173.78
Buy & Hold Final: $2,240.58
Total Return: -16.5%
Buy&Hold Return: -55.2%
Volatility: 21.9%
B&H Volatility: 66.3%
Max Drawdown: 19.9%
Saved charts to crypto_trading_results/

===== Analyzing AVAX-USD =====
Records: 181
First: $39.01 | Last: $16.67 | Change: -57.3%
Strategy Final: $3,972.46
Buy & Hold Final: $2,136.10
Total Return: -20.5%
Buy&Hold Return: -57.3%
Volatility: 24.9%
B&H Volatility: 78.9%
Max Drawdown: 26.1%
Saved charts to crypto_trading_results/

===== Analyzing MATIC-USD =====
Records: 181
First: $0.50 | Last: $0.17 | Change: -65.5%
Strategy Final: $4,104.68
Buy & Hold Final: $1,724.32
Total Return: -17.9%
Buy&Hold Return: -65.5%
Volatility: 19.6%
B&H Volatility: 69.3%
Max Drawdown: 20.7%
Saved charts to crypto_trading_results/

===== Analyzing SHIB-USD =====
Records: 181
First: $0.00 | Last: $0.00 | Change: -51.9%
Strategy Final: $3,741.33
Buy & Hold Final: $2,404.19
Total Return: -25.2%
Buy&Hold Return: -51.9%
Volatility: 23.2%
B&H Volatility: 68.1%
Max Drawdown: 27.8%
Saved charts to crypto_trading_results/

===== Analyzing TRX-USD =====
Records: 181
First: $0.25 | Last: $0.27 | Change: 7.2%
Strategy Final: $4,633.83
Buy & Hold Final: $5,361.75
Total Return: -7.3%
Buy&Hold Return: 7.2%
Volatility: 19.6%
B&H Volatility: 38.1%
Max Drawdown: 23.4%
Saved charts to crypto_trading_results/

===== Analyzing LINK-USD =====
Records: 181
First: $24.45 | Last: $11.89 | Change: -51.3%
Strategy Final: $3,928.07
Buy & Hold Final: $2,432.87
Total Return: -21.4%
Buy&Hold Return: -51.3%
Volatility: 25.4%
B&H Volatility: 77.7%
Max Drawdown: 23.5%
Saved charts to crypto_trading_results/

===== Analyzing ATOM-USD =====
Records: 181
First: $6.93 | Last: $3.76 | Change: -45.7%
Strategy Final: $3,309.85
Buy & Hold Final: $2,714.44
Total Return: -33.8%
Buy&Hold Return: -45.7%
Volatility: 19.8%
B&H Volatility: 69.0%
Max Drawdown: 33.8%
Saved charts to crypto_trading_results/

==================================================
ANALYSIS COMPLETE IN 291.9 SECONDS
==================================================
```

## Notebook/Script Structure
```text
# Crypto Data Fetcher
├── COIN_IDS = { ... }  # 15 major cryptocurrencies
└── fetch_market_data(assets, start_date, end_date) # Smart rate limiting with header-based cooldowns, Robust error handling for API failures, Professional OHLC data processing

# Trading Signals Generator 
├── generate_signals(data, short=12, long=26) # EMA(12) and EMA(26) calculations, Volatility-based position sizing (14-day std)
    └── position_size = 1 - min(daily_vol * 10, 0.8)

# Portfolio Simulator
└── simulate_strategy(data, signals, capital=5000) # Realistic 0.1% trading fee implementation, Strategy vs Buy & Hold comparison, Look-ahead bias prevention (position.shift(1))

# Trading Visualizer
├── plot_price_signals(data, signals, symbol, output_dir) # EMA crossover markers with entry/exit signals
└── plot_performance_comparison(portfolio, symbol, output_dir) # Annotated final values with clean formatting

# Performance Analytics
└── calculate_metrics(portfolio) # Total Return, Annualized Volatility, Max Drawdown, Buy & Hold comparison

# Main Execution
└── __main__ # Configuration setup, Data pipeline orchestration, Results reporting
```
## Examples
### ADA-USD
![ADA-USD_performance_20250622_0208](https://github.com/user-attachments/assets/a544f688-b754-4017-98c0-2786f9031b40)
![ADA-USD_signals_20250622_0208](https://github.com/user-attachments/assets/7023ed65-582a-44dc-bca5-5b5d5f59f777)

### ATOM-USD
![ATOM-USD_performance_20250622_0208](https://github.com/user-attachments/assets/a2957e2b-c00f-4797-99e0-40c2329c37d0)
![ATOM-USD_signals_20250622_0208](https://github.com/user-attachments/assets/5749b400-95a9-47d9-9536-dd07fbbce0ac)

### AVAX-USD
![AVAX-USD_performance_20250622_0208](https://github.com/user-attachments/assets/0a461b2a-f334-4c62-8fd2-7221697e5dbf)
![AVAX-USD_signals_20250622_0208](https://github.com/user-attachments/assets/04347d47-2612-44fe-bbd6-aafa295a7bdc)

### BNB-USD
![BNB-USD_performance_20250622_0208](https://github.com/user-attachments/assets/26d10ed4-ffd2-4d7a-9567-48a179fef893)
![BNB-USD_signals_20250622_0208](https://github.com/user-attachments/assets/e26a12d7-3f57-44cd-95f9-317ff97beda5)

### BTC-USD
![BTC-USD_performance_20250622_0208](https://github.com/user-attachments/assets/f047ad7a-69c9-47af-aad9-6c674955dcbd)
![BTC-USD_signals_20250622_0208](https://github.com/user-attachments/assets/dc12d60c-5358-4a7f-883d-a4c32332424e)

### DOT-USD
![DOT-USD_performance_20250622_0208](https://github.com/user-attachments/assets/775a7945-f986-49a0-a944-1b41ea886690)
![DOT-USD_signals_20250622_0208](https://github.com/user-attachments/assets/9b72542e-9742-4043-bfff-6c87307d440f)

### DOGE-USD
![DOGE-USD_performance_20250622_0208](https://github.com/user-attachments/assets/171b8f82-143b-43bd-9194-c14b60a57dad)
![DOGE-USD_signals_20250622_0208](https://github.com/user-attachments/assets/1d8f00c7-81d5-408b-99b7-43626ad26227)

### ETH-USD
![ETH-USD_performance_20250622_0208](https://github.com/user-attachments/assets/16d2eba3-b83c-491a-a810-92fe05b65269)
![ETH-USD_signals_20250622_0208](https://github.com/user-attachments/assets/2939c9bd-5f96-4ecd-b378-fecc0a70c01d)

### LINK-USD
![LINK-USD_performance_20250622_0208](https://github.com/user-attachments/assets/d805fd00-cf2d-4028-8a72-a1eac55eb144)
![LINK-USD_signals_20250622_0208](https://github.com/user-attachments/assets/fed08d35-09d8-4c95-805b-2494a77f9a06)

### LTC-USD
![LTC-USD_performance_20250622_0208](https://github.com/user-attachments/assets/3b7a5b88-3c15-4011-9267-b3645f08d500)
![LTC-USD_signals_20250622_0208](https://github.com/user-attachments/assets/d14bee13-d999-47e7-8925-496ecbb48522)

### MATIC-USD
![MATIC-USD_performance_20250622_0208](https://github.com/user-attachments/assets/502f1891-8094-4d6a-8a6b-fd589e9a3041)
![MATIC-USD_signals_20250622_0208](https://github.com/user-attachments/assets/3e4d2052-bf03-4d2d-8d25-f87515bcdc21)

### SHIB-USD
![SHIB-USD_performance_20250622_0208](https://github.com/user-attachments/assets/d0c59df3-0cc4-4e86-a8d5-998a5070a79a)
![SHIB-USD_signals_20250622_0208](https://github.com/user-attachments/assets/5536f5b9-8acc-4c8b-9eaa-cd56cf92c553)

### SOL-USD
![SOL-USD_performance_20250622_0208](https://github.com/user-attachments/assets/41dae2ee-9601-4f87-953c-d9659a3bc8d3)
![SOL-USD_signals_20250622_0208](https://github.com/user-attachments/assets/42434a13-c682-4f0f-9af7-d02f571d7107)

### TRX-USD
![TRX-USD_performance_20250622_0208](https://github.com/user-attachments/assets/8212a592-aa1a-4283-9416-b059e2aa3a76)
![TRX-USD_signals_20250622_0208](https://github.com/user-attachments/assets/9f8f1b24-e19f-401e-9cab-bc92d6080ba3)

### XRP-USD
![XRP-USD_performance_20250622_0208](https://github.com/user-attachments/assets/6a206949-7eb7-4646-a4c6-d9dcc74a14f3)
![XRP-USD_signals_20250622_0208](https://github.com/user-attachments/assets/a5958cbf-efc3-4746-b392-9415f5c4b72c)


## Risk Disclosure
Cryptocurrency trading involves substantial risk of loss and is not suitable for every investor. Past performance is not indicative of future results. This system is for educational purposes only and should not be considered financial advice.

Note: This is a simulation framework only - not financial advice. Always test strategies with historical data before live trading.

---

## License
This project is licensed under the MIT License. See LICENSE file for details.
