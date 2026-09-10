# Ghostfolio Community Edition [for Windows] 


---

## Welcome!

This is your comprehensive guide to **Ghostfolio Community Edition** — a 100% free, open-source wealth management desktop environment for tracking personal finances, stocks, ETFs, crypto, and asset allocation.

As a **Self-Hosted application** running locally on your machine, it completely eliminates the need for expensive monthly subscriptions. It operates entirely independent of third-party cloud servers, ensuring that your financial footprint remains strictly your own.

---


## What You Get in This Build

-  **Absolute Privacy** — 100% local data storage with zero telemetry, trackers, or cloud leaks
-  **Multi-Asset Tracking** — monitor stocks, ETFs, crypto, cash accounts, and precious metals
-  **Automatic Price Feeds** — integrated with free market data providers (Coingecko, Yahoo Finance)
-  **Advanced Analytics** — dynamic tracking of net worth evolution and performance metrics (TWR, MWR)
-  **Seamless Import** — robust support for loading transaction history via CSV files from brokers and exchanges
-  **Multi-User Support** — set up independent, isolated accounts for your family members
-  **Open REST API** — unlimited API access to automate or log trades from external scripts (n8n, Node-RED)
-  **Self-Hosted Freedom** — completely ad-free, restriction-free software that costs $0 forever

---

## Windows Compatibility

| OS / Environment | Status | Requirements |
|-----------------|:------:|:------:|
| Windows 10 (with Docker Desktop) |  Fully Supported | WSL 2 enabled, Virtualization active in BIOS |
| Windows 11 (with Docker Desktop) |  Fully Supported | WSL 2 enabled, Virtualization active in BIOS |

**System Requirements:**
- Processor: Intel i3 / AMD Ryzen 3 or newer
- RAM: 4GB minimum (The Ghostfolio Docker container footprint is very light, using only ~150–250MB)
- Storage: 500MB free disk space (allocated for the PostgreSQL database volumes)
- Internet: Active connection required for standard container deployment and market rate updates

---

## How to Install on Windows

### Step 1: Prepare the Environment
- Download and install **Docker Desktop for Windows** from the official website.
- Verify that **WSL 2** (Windows Subsystem for Linux) is fully updated and running on your system.

### Step 2: Create Your Configuration Directory
- Create a dedicated folder on your hard drive (e.g., `C:\Ghostfolio`).
- Inside this folder, create a plain text file named `docker-compose.yml`.
- Populate it with the standard `ghostfolio` and `postgres` database container setup recipes.

### Step 3: Spin Up the Containers
- Open a terminal (PowerShell or Command Prompt) directly inside your directory.
- Execute the launch command: `docker compose up -d`.
- Wait a brief moment (1–2 minutes) for Docker to pull the images and launch the background database.

### Step 4: Access the Local Dashboard
- Launch any web browser and navigate to: `http://localhost:3333`.
- Follow the prompt to create an administrator profile and select your primary account currency.

---

## Platform Capabilities

### Portfolio Monitoring
- Keep an explicit ledger of global stocks, index-tracking exchange-traded funds (ETFs), and trusts.
- Comprehensive coverage of decentralized digital assets, major cryptocurrencies, and stablecoins.
- Track liquid cash reserves, traditional checking/savings accounts, and commodities like physical gold.
- Organize asset distribution visually across specific market sectors, asset classes, and global regions.

### Quantitative Analytics
- Calculate real-time Time-Weighted Rate of Return (TWR) and Money-Weighted Rate of Return (MWR).
- Compare your net performance directly against traditional market indices (such as the S&P 500).
- Transparent auditing for cash dividends, token distributions, trade transaction fees, and corporate stock splits.
- Utilize customizable visual charts to enforce strict baseline target weights for rebalancing.

### Infrastructure & Security
- Backed by an enterprise-ready local PostgreSQL instance, safely confined behind your system file permissions.
- State management and authentication secured through encrypted JSON Web Tokens (JWT).
- Generate custom API bearer keys to securely push incoming transactions via external automation scripts.
- Dead-simple manual backups: simply copy or archive your persistent Docker database volume folder.

---

## Comparison: Cloud Trackers vs Local Ghostfolio

| Feature | Third-Party Cloud Services | Ghostfolio Community Edition |
|---------|:------:|:------:|
| Data Storage | External servers (vulnerable to breaches) |  **100% Local & anonymous** |
| Ads & Telemetry | Highly prevalent on free tiers |  **Completely absent** |
| Geopolitical Geofencing | Susceptible to server/regional bans |  **Unbannable & permanent** |
| API Rate Limits | Throttled unless paying premium fees |  **Completely unlimited REST API** |
| Export Boundaries | Locked or restricted behind paywalls |  **Total programmatic control over DB** |
| Software Cost | High monthly/yearly subscriptions |  **$0 Forever (Open-Source)** |

---

## Important Notes

### Local Network Access
- Out of the box, your dashboard is bound to `localhost:3333` for standalone access.
- To access your portfolio from a mobile device on your home Wi-Fi network, add an inbound port rule to your Windows Defender Firewall.

### Regular Backups
- Ensure you periodically export your raw transactional legwork via the native web CSV export option, or preserve regular cold file copies of your local Docker volumes.

---

## Troubleshooting

### Common Deployment Issues

**The app container crashes with a database error**
- Double-check that your default PostgreSQL connection port (typically 5432) isn't being bound by an independent native Postgres server running locally on Windows.
- Ensure the structural alignment of database passwords across matching environment values (`POSTGRES_PASSWORD`).

**The web application at `localhost:3333` fails to connect**
- Bring up the Docker Desktop graphical application and verify that all service lights are running green.
- Investigate internal runtime events by calling up execution output using `docker compose logs`.

---

## Post-Installation Checklist

Upon your very first login, it is highly recommended to do the following:

1.  Formulate a strong master administrative password.
2.  Assign your default base ledger currency (USD, EUR, GBP, etc.).
3.  Manually test a mock asset purchase entry (e.g., a fraction of BTC or a share of AAPL).
4.  Confirm that downstream background trackers are correctly pulling current asset pricing metrics.
5.  Configure custom mappings to ingest historic transaction CSV exports if transferring an active portfolio.

---

## Community & Support

- **GitHub Issues:** File formal bugs and report interface errors directly to the core developers.
- **GitHub Discussions:** Join global forums regarding community integrations, custom scrapers, and strategic financial layouts.
- **Documentation:** Review deep-dive software architectural walk-throughs over at `docs.ghostfolio.org`.

---

## Disclaimer

This platform serves strictly as a personal financial database optimization utility. The software is provided under the terms of the AGPL-3.0 License "as-is", without warranties or liabilities of any manner. The authoring community assumes zero accountability for personal investment actions or prospective market downswings.

---

## License

This application repository and deployment documentation are formally made available under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

---

**Thank you for choosing private, sovereign financial auditing with Ghostfolio Community Edition!**
