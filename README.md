# Advanced Cryptocurrency Trading System

Professional-grade crypto trading algorithm leveraging CoinGecko's free API. Features multi-asset support, technical indicators, backtesting framework, and performance analytics with robust rate limit handling.
This is more like an enhanced cryptocurrency trading system with these key upgrades from the original Yahoo Finance-based version which can be found in this github repository: https://github.com/johnnietse/cryptocurrency-trading-system.git

## 🔑 Key Features
- **Multi-Asset Support**: Analyze 15+ major cryptocurrencies (BTC, ETH, SOL, etc.) and up to 28+ cryptocurrencies are supported by CoinGecko's API
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
