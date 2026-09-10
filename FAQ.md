# Frequently Asked Questions (FAQ) - Ghostfolio Community Edition

## General Questions

### Q: Is Ghostfolio Community Edition really free forever?
**A:** Yes! Ghostfolio Community Edition is an **open-source project** distributed under the GNU Affero General Public License v3.0 (AGPL-3.0). All features are permanently unlocked with **no recurring payments, premium tiers, subscriptions, or hidden fees**.

### Q: Can I run Ghostfolio on Windows?
**A:** **Yes!** While Ghostfolio is a web application, it can be seamlessly deployed on **Windows 10 and Windows 11** using Docker Desktop. You can also host it on macOS, Linux, or a dedicated home server.

### Q: Where can I find the official source code?
**A:** The project is fully transparent and maintained publicly on GitHub. You can inspect the source code, contribute, or build it yourself directly from the official repositories.

### Q: Will I lose access to my financial data?
**A:** No! Your transaction history, accounts, and portfolio preferences are **stored locally on your own machine** within your database volumes. You maintain 100% ownership and absolute control over your financial data.

---

## Installation & Setup (via Docker Desktop)

### Q: What are the system requirements for Windows?
**A:**
- **OS:** Windows 10 or Windows 11 (with WSL 2 backend enabled)
- **RAM:** Minimum 4GB (The Ghostfolio stack is lightweight, consuming only ~150MB–250MB)
- **Storage:** 500MB free disk space for the local PostgreSQL database volumes
- **Processor:** Intel i3 / AMD Ryzen 3 or newer
- **Virtualization:** Enabled in your system BIOS/UEFI
- **Tools:** Docker Desktop for Windows installed and running

### Q: How do I spin up Ghostfolio?
**A:**
1. Create a dedicated folder (e.g., `C:\Ghostfolio`).
2. Create a plain text file named `docker-compose.yml` inside that folder.
3. Paste the official Ghostfolio multi-container configuration (App + PostgreSQL database) into the file.
4. Open PowerShell or Command Prompt in that directory and run: `docker compose up -d`
5. Open your web browser and navigate to `http://localhost:3333`.

### Q: Do I need to activate a license or enter API keys?
**A:** No! The platform comes fully unlocked. You only need to create a **local master administrator account** upon your first launch to secure your dashboard.

### Q: How long does the installation take?
**A:** Typically **1–3 minutes**. It depends entirely on your internet download speed to pull the official container images from Docker Hub for the first time.

### Q: What if the container fails to start or crashes?
**A:**
1. Ensure **Docker Desktop** is active and running in the background.
2. Verify that local port `3333` or database port `5432` is not already occupied by another local service on your Windows machine.
3. Run `docker compose logs` in your terminal to inspect explicit database connection or permission errors.

---

## Features & Usage

### Q: What financial assets can I track?
**A:** 
-  **Global Stocks & ETFs** (US, European, Asian, and emerging markets)
-  **Cryptocurrencies & Stablecoins** (Bitcoin, Ethereum, DeFi tokens, etc.)
-  **Liquid Cash & Commodities** (Multiple fiat currencies, bank accounts, physical gold/silver)

### Q: How are market price feeds updated?
**A:** Ghostfolio aggregates real-time and historical pricing metrics automatically using free, built-in open integrations like **Yahoo Finance** and **CoinGecko**.

### Q: Can I calculate advanced portfolio returns?
**A:** Yes! The platform calculates professional-grade metrics, including **Time-Weighted Rate of Return (TWR)** and **Money-Weighted Rate of Return (MWR)**, factoring in cash drag, commissions, and dividend payouts.

### Q: Is there an automated import option?
**A:** Yes! You can easily batch-upload your historic transaction legwork using native **CSV import templates** mapped to popular brokers, banks, and crypto exchanges.

### Q: Is full API access included?
**A:** Yes! Ghostfolio features a fully documented local **REST API**. You can generate custom bearer tokens in your settings to programmatically log transactions from scripts or automation platforms (like n8n or Node-RED).

---

## Security & Privacy

### Q: Is my financial data secure?
**A:** 
- **100% Private:** Your net worth, asset quantities, and trading history are never transmitted to corporate trackers or cloud servers.
- **Local Control:** All data processing occurs on your physical machine inside the sandboxed Docker network.
- **Secure Sessions:** Account authentication and dashboard access are validated using local JSON Web Tokens (JWT).

### Q: Is my trading data shared with anyone?
**A:** No! Since the platform is self-hosted, no third party has visibility into your assets. There are no tracking scripts, telemetry reporting, or corporate analytical engines included.

### Q: Can I run Ghostfolio over a VPN?
**A:** Yes! Ghostfolio supports standard VPN configurations seamlessly. You can also securely access your local instance remotely by setting up a private home network tunnel (such as WireGuard or Tailscale).

---

## Updates & Maintenance

### Q: How do I update to the latest version?
**A:**
Updating a self-hosted Docker instance takes less than a minute. Open your terminal in your configuration folder and run:
```bash
docker compose pull
docker compose up -d
```
This pulls down the latest code changes while completely preserving your persistent database volumes.

### Q: Are software updates free?
**A:** Yes! Every single release, security patch, and community-driven feature enhancement is completely free.

---

## Integration & Automation

### Q: Can I sync this directly with my live brokerage account?
**A:** To maximize security and protect your privacy, Ghostfolio avoids direct, persistent syncing connections to live bank accounts. Instead, it relies on clean CSV imports or programmatic logging via the open REST API.

### Q: Does it support multi-user environments?
**A:** Yes! You can enable multi-account profiles in the configuration, allowing family members to create separate, private, and fully isolated financial portfolios on a single local server deployment.

---

## Community & Support

### Q: How do I report a software bug?
**A:** You can submit formal issues, feature requests, or UI bug reports directly onto the main project repository's **GitHub Issues** page.

### Q: Where can I ask questions about advanced setups?
**A:** Check out **GitHub Discussions** or join the official community channels to swap deployment advice, custom CSV parser scripts, and rebalancing strategies with other users.

---

## Disclaimer

### Q: What is the legal disclaimer?
**A:** Ghostfolio is an open-source data aggregation utility intended strictly for educational, organizational, and personal research purposes. It does not provide financial, legal, or investment advice. All financial tracking and investment decisions are carried out completely at your own risk.

---

## Getting Started

### Q: What should I do immediately after my first login?
**A:**
1. Secure your master administrator account with a robust password.
2. Select your base display currency (e.g., USD, EUR, GBP).
3. Test a single mock asset manual transaction (e.g., purchasing 1 share of AAPL or 0.1 BTC).
4. Verify that the system successfully fetches the asset details and current market price.
5. Review the official documentation at `docs.ghostfolio.org` to set up automated CSV imports.

---

**Last Updated:** 2026  
**License:** GNU AGPLv3 (Open Source)  
**Platform Deployment:** Windows 10 / Windows 11 (via Docker Desktop)  
**Cost:** $0 Forever
