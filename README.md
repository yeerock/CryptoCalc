# Crypto Profit Calculator

A powerful, real-time trading companion with a native iOS aesthetic, running entirely in your browser. Track multiple buy orders, visualize potential profits on an interactive chart, and sync your data seamlessly across devices.

### [➡️ View Live Demo](https://yeerock.github.io/CryptoCalc/)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![VueJS](https://img.shields.io/badge/vue.js-3.x-brightgreen.svg)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-3.x-blue.svg)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-purple.svg)

![CryptoCalc Desktop Screenshot](https://yeerock.github.io/CryptoCalc/desktop-screenshot.png)

Tired of manual spreadsheet calculations and delayed data? This Crypto Profit Calculator is designed to be your go-to tool for on-the-fly trade analysis. It's built as a single-page application that leverages your browser's local storage, meaning your data is private, persistent, and requires no backend or user accounts.

---

## ✨ Core Features

### The Real-Time Dashboard
<img src="https://yeerock.github.io/CryptoCalc/mobile-screenshot.png" alt="Mobile Dashboard View" width="320" align="right" style="margin-left: 20px; border-radius: 10px;"/>

Get an instant, comprehensive overview of your trading position. The main dashboard is designed for clarity and quick insights, providing all critical information at a glance.

-   **Live Price Ticker**: The current price of your selected asset, fetched from the Binance API every second and animated to draw your attention to changes.
-   **Instant Profit/Loss Calculation**: See your net profit in USDT, your local currency (MYR), and as a percentage, updated in real-time as the market moves.
-   **Detailed Summary**: A clear breakdown of your total investment, fees paid, average buy price, and the total coins you've acquired.
-   **Market Pressure Gauge**: A live visualization of buy vs. sell pressure from the order book, helping you gauge immediate market sentiment.

<br clear="right"/>

### Interactive Profit Charting

Visualize your profit potential over time. The integrated chart is more than just a static image; it's a dynamic tool for analyzing how price fluctuations impact your bottom line.

-   **Dynamic Time Ranges**: Switch between views from 5 minutes to 7 days to see both short-term volatility and long-term trends.
-   **Color-Coded Gains/Losses**: The chart line automatically changes color from green (profit) to red (loss), making it easy to see your break-even point.
-   **Detailed Tooltips**: Hover over the chart to see the exact profit/loss, coin price, and timestamp for any point in time.
-   **Persistent History**: Chart data is saved to your browser's IndexedDB, so your profit history persists across sessions.

![Profit Chart Screenshot](https://yeerock.github.io/CryptoCalc/profitchart-screenshot.png)

### Seamless Data Sync with QR Codes
<img src="https://yeerock.github.io/CryptoCalc/sharingqr-screenshot.png" alt="QR Code Sharing Modal" width="320" align="left" style="margin-right: 20px; border-radius: 10px;"/>

Stop re-entering your trade data on different devices. This unique feature allows you to export your entire configuration—including all buy orders, fee settings, and selected coin—into a single QR code.

Simply scan the QR code with another device (like your phone or tablet) to instantly import the complete setup. It's the perfect way to sync your data between your desktop and mobile devices without a server.

<br clear="left"/>

### And Much More...

-   **🔀 Multi-Order Averaging**: Add unlimited buy orders, and the app will automatically calculate your weighted average buy price.
-   **💾 Persistent Local Storage**: All your data is saved securely in your browser's IndexedDB. It persists between sessions and is automatically loaded when you return.
-   **🔔 Customizable Price Alerts**: Set a price threshold (e.g., $500) and receive a visual, audio, and vibration notification every time the price crosses a multiple of that value.
-   **📱 PWA Ready**: Optimized for mobile and can be "Added to Home Screen" on iOS and Android for a fast, full-screen, app-like experience.
-   **🚀 Zero Backend**: The entire application is a single `index.php` file that runs entirely on the client-side. Your data never leaves your device.

---

## 🛠️ Technology Stack

This project is built with modern, lightweight web technologies, all served via CDNs for simplicity and speed.

-   **Framework**: [Vue.js 3](https://vuejs.org/)
-   **Styling**: [Tailwind CSS](https://tailwindcss.com/)
-   **Charting**: [Chart.js](https://www.chartjs.org/) with `chartjs-adapter-date-fns`
-   **QR Code Generation**: `qrcode.js`
-   **QR Code Scanning**: `html5-qrcode`
-   **Client-Side Storage**: [IndexedDB API](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)
-   **Data Source**: [Binance Public API](https://github.com/binance/binance-spot-api-docs)

---

## 🚀 Getting Started

The application is designed to be intuitive. Here’s a typical workflow:

1.  **Select Your Coin**: Navigate to the **Settings** tab and choose the cryptocurrency you are trading (e.g., ETH, BTC).
2.  **Enter Buy Orders**: Go to the **Buy Orders** tab. Enter the `Price` and `USDT` amount for each of your buy orders. The app will calculate your average cost basis automatically.
3.  **Set Your Target**: In the **Sell Order** tab, enter your desired selling price or toggle "Real-time Price" to track the market.
4.  **Analyze Results**: Return to the **Home** tab to see your complete profit summary and watch the live chart.

---

## 💻 Local Development & Setup

Since this is a single-file application with no build process, setting it up locally is extremely simple.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yeerock/CryptoCalc.git
    cd CryptoCalc
    ```
2.  **Serve the file:**
    The file is named `index.php`, but it contains no server-side PHP code. You can rename it to `index.html`. You'll need a local web server to prevent potential CORS issues when the app calls the Binance API.

    *   **Using Python's built-in server:**
        ```bash
        # Python 3
        python -m http.server 8000
        ```
    *   **Using VS Code's Live Server extension:**
        Right-click the `index.php` file and choose "Open with Live Server".

3.  **Open in your browser:**
    Navigate to `http://localhost:8000`. You're all set!

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for new features, bug fixes, or UI improvements, please feel free to:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-awesome-feature`).
3.  Make your changes.
4.  Commit your changes (`git commit -m 'Add some awesome feature'`).
5.  Push to the branch (`git push origin feature/your-awesome-feature`).
6.  Open a Pull Request.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
