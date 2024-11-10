🌐 Live Order Book Heatmap 🚀

Visualize Limit Orders and Market Activity in Real-Time! 📊🔮

This live order book heatmap is a real-time tool for traders and enthusiasts that allows you to visualize the flow of limit orders and market activity in an interactive and user-friendly way. Built using Binance WebSocket API, this tool brings you up-to-the-minute data with dynamic heatmaps, order book graphs, and time & sales logs.

👉 Note: Best suited for less volatile markets — perfect for analyzing stable assets! If you're seeing performance issues, feel free to adjust the update interval or reduce the heatmap size. 🔧
🔥 Key Features 💡

    Limit Order Heatmap: The heatmap provides a visual representation of resting limit orders. Higher liquidity at certain price levels is shown with brighter colors 🔴🟢, making it easy to spot where the market is likely to face resistance or support.

    Market Order Circles: Circle sizes represent the number of contracts traded in the past period, while their colors 🌈 show the buy vs. sell activity. Larger circles = more market orders, and the color intensity shows the buy/sell ratio. 🛒📈

    Interactive Time & Sales Log: See the top 10% of orders (by size) highlighted in a dedicated log, giving you a glimpse into major market moves. 📜

    Flexible Visualizations: Choose between linear vs logarithmic color scales, two vibrant color themes 🌟, and customizable update intervals. Perfect for various trading symbols 🔄.

🛠️ Tech Stack 💻

    Binance WebSocket API: Real-time data feed from Binance. 📡🔌

    D3.js Visualizations: Interactive charts, heatmaps, and more, using SVG for sharp, scalable graphics. 🔮📉

    Tick.js: Handle price data without any rounding errors. It keeps things accurate and precise! 🧮🔍

📦 Structure Breakdown 🛠️
1. lib/BinanceDataFeed.js

Handles real-time market data via the Binance WebSocket API. A super easy-to-use client that allows you to subscribe to various data streams (like trades or order book updates). 🧑‍💻

Example:

feed.subscribe('BTCUSDT', {
  onTrade: (data) => console.log(data)
});

2. lib/BinanceOrderBook.js

This is the heart of the heatmap! It manages the live order book and calculates important stats. It also fetches the order book snapshots for visual representation. 📚📊
3. lib/Tick.js

💡 Did you know? Binance returns prices as strings. Tick.js works with these strings, converting them into accurate, precise numbers for calculations — no rounding errors! 🔧
4. src/Dashboard.js

The dashboard integrates everything and provides an easy-to-use interface for displaying heatmaps, order graphs, and more. 🖥️✨
🔄 Performance Tips ⚡

    For less volatile markets, this tool works great. However, if you’re dealing with highly volatile markets, performance might dip. To improve performance, you can lower the update interval or reduce the heatmap size. 🔍

    SVG to Canvas Switch: Replacing SVGs with canvas elements will drastically improve rendering performance. 🏎️💨

🚀 Quick Start Guide 🏁

Ready to dive in? 🚀 Here’s how to get started:

    Clone the Repo: Get your hands on the code! 🎯

    git clone https://github.com/elenchev/Real-Time-Order-Book-Heatmap-and-Market-Data-Visualization.git


    Set Up Your Environment: Follow the setup instructions in the repo to get your environment ready. 🛠️

    Start Visualizing: Choose your favorite market (e.g., BTC/USDT), and watch the magic happen as real-time data feeds into the heatmap. 🌍🔥

⚡ Future Updates ✨

    Enhanced Handling of Volatile Markets: We’ll implement aggregated price support for more stability in choppy markets. 📉

    Canvas Optimizations: Canvas elements are coming soon to make visualizations even faster! 🖼️⚡

🚨 Important Notes ⚠️

    🔑 API Timeouts: The datafeed doesn't handle long connections, so your connection may timeout after 1 hour. This is intended to avoid the complexity of managing credentials.

    📊 Less Volatility = Better Performance: Highly volatile markets can make the heatmap less reliable. This can be improved with aggregated data, which is already supported — just not yet implemented in the current version.

Take your trading analysis to the next level with our real-time heatmap and order book insights! 🚀📊 Whether you’re a casual trader or a seasoned pro, this tool gives you a visual edge. 🔥

4. Start Visualizing:

That's it! The heatmap will now show real-time market data, allowing you to track orders, trades, and liquidity in the market. 🌍📊

Now you're all set! Just follow these steps, and you're ready to start visualizing live market data! 🚀🎉

⚡ Future Updates ✨

    Enhanced Handling of Volatile Markets: We’ll implement aggregated price support for more stability in choppy markets. 📉

    Canvas Optimizations: Canvas elements are coming soon to make visualizations even faster! 🖼️⚡

🚨 Important Notes ⚠️

    🔑 API Timeouts: The datafeed doesn't handle long connections, so your connection may timeout after 1 hour. This is intended to avoid the complexity of managing credentials.

    📊 Less Volatility = Better Performance: Highly volatile markets can make the heatmap less reliable. This can be improved with aggregated data, which is already supported — just not yet implemented in the current version.

Take your trading analysis to the next level with our real-time heatmap and order book insights! 🚀📊 Whether you’re a casual trader or a seasoned pro, this tool gives you a visual edge. 🔥

