# QuantFin Analytics Dashboard

Enhanced Sentio dashboard configuration with Average Daily Gain metrics for BlueFin Perps trading analysis.

# Credits to evandekim for this beautiful dashboard! I am just helping keep it maintained add functionality.

## Features

### Original Panels
- **Cumulative Volume (Per Market)**: Shows running total of volume by market
- **Daily Volume Per Market**: Daily trading volume breakdown
- **Order Sizes**: Scatter plot of margin usage over time
- **Largest Positions Executed (Daily)**: Daily maximum position sizes
- **Cumulative Trading Stats**: Overall trading performance metrics
- **Daily Data Per Market**: Detailed daily trading data table

### New Average Daily Gain Panels
- **Average Daily Gain**: Line chart showing daily gain percentages with 7-day moving average
- **Cumulative Performance**: Bar chart showing cumulative gain percentage over time

## SQL Queries

### Average Daily Gain Calculation
The new panels calculate daily gains based on:
- Daily PnL from realized trades (sells minus buys)
- Daily gain percentage = (daily_pnl / daily_volume) * 100
- 7-day moving average for trend analysis
- Cumulative performance tracking

### Key Metrics
- **Daily Gain %**: Percentage return for each trading day
- **7-Day Moving Average**: Smoothed trend line
- **Cumulative Gain %**: Running total performance
- **Daily Return %**: Individual day performance

## Usage

1. Import the `dashboard_config.json` into your Sentio dashboard
2. Ensure the `$address` parameter is set to your trading address
3. The dashboard will automatically calculate and display average daily gains

## Trading Address
Currently configured for: `0x3753041ccba494b0006edaf552c9d78bf680827bf18b2e3004c4c8c447eba095`

## Markets Supported
- BTC-PERP
- ETH-PERP
- All other BlueFin perpetual markets
