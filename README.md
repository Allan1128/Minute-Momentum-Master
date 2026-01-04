Minute-Momentum-Master ⚡
Ultra-fast 1-minute perpetual contract scalping bot designed for high-frequency cryptocurrency trading. Captures micro-trends and momentum shifts on the shortest timeframes with precision execution.

📋 Quick Overview
Strategy: High-frequency momentum scalping

Timeframe: 1-minute charts exclusively

Instruments: Perpetual contracts (swap)

Target: 0.3-0.8% profit per trade

Risk: Ultra-tight 0.5% stop loss

✨ Core Features
⚡ Trading Engine
Ultra-fast EMA crosses (5, 10, 20 periods)

VWAP-based entry timing

Bollinger Band squeeze detection

RSI mean reversion signals

Real-time order book analysis

🛡️ Risk Management
0.5% maximum stop loss

0.8% take profit target

1-2% position sizing

Auto-position management

Spread monitoring

🔧 Technical Stack
OKX perpetual contracts integration

CCXT library for exchange connectivity

Sub-minute execution cycles

Comprehensive logging system

Production-ready error handling

🚀 Quick Start
Prerequisites
bash
Python 3.8+
OKX API with perpetual trading permissions
Installation
bash
git clone https://github.com/Allan1128/Minute-Momentum-Master.git
cd Minute-Momentum-Master
pip install ccxt pandas numpy
cp config.example.json config.json
# Edit config.json with your OKX API credentials
Configuration
json
{
  "api_key": "your_okx_api_key",
  "api_secret": "your_okx_api_secret",
  "passphrase": "your_passphrase",
  "symbols": ["BTC/USDT", "ETH/USDT"],
  "test_mode": true,
  "risk_per_trade": 0.01
}
Run the Bot
bash
# Start in test mode (recommended)
python Minute-Momentum-Master.py

# Run specific symbols
python Minute-Momentum-Master.py --symbols BTC/USDT

# Custom interval (default 60 seconds)
python Minute-Momentum-Master.py --interval 30
📈 Strategy Logic
Entry Signals
Momentum Confirmation: EMA(5) > EMA(10) > EMA(20)

Volume Surge: Current volume > 150% of 20-period average

RSI Position: RSI between 35-65 (not extreme)

Order Flow: Bid-ask imbalance > |0.1|

VWAP Alignment: Price above VWAP for longs, below for shorts

Exit Conditions
Profit Target: 0.8% from entry

Stop Loss: 0.5% from entry

Time Exit: 3 minutes maximum hold

Trailing Stop: Activates after 0.4% profit

⚙️ Customization
Adjust Parameters
python
# In main() function
STOP_LOSS_PCT = 0.005     # 0.5%
TAKE_PROFIT_PCT = 0.008   # 0.8%
MAX_HOLD_MINUTES = 3      # Maximum position duration
MIN_SIGNAL_STRENGTH = 2.5 # Minimum signal strength to trade
Modify Indicators
python
def customize_indicators(self, df):
    # Add your custom indicators
    df['custom_signal'] = your_calculation(df)
    return df
📊 Performance Tracking
Log Files
scalping_orders.json: Complete trade history

Console: Real-time signal output

Performance metrics after each cycle

Key Metrics
Win rate percentage

Average profit per trade

Maximum drawdown

Sharpe ratio approximation

Trade frequency per hour

⚠️ Critical Warnings
High-Risk Nature
EXTREME RISK: High-frequency trading magnifies losses

Requires constant monitoring: Not automated investing

Exchange fees critical: High turnover affects profitability

Latency sensitive: Server location impacts performance

Best Practices
Start with simulated trading for at least 1 week

Use minimal capital (100-500 USDT recommended)

Monitor closely during first live sessions

Adjust parameters based on market conditions

Keep detailed logs for analysis

🎯 Ideal Market Conditions
High volatility (>3% daily range)

Strong directional trends

Normal to high liquidity

Low network congestion

Active trading sessions (Asia, Europe, US overlaps)
OKX Invitation: https://www.growthnode.systems/join/59892411
