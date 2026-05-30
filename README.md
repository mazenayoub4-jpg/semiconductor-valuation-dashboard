# semiconductor-valuation-dashboard
Power BI dashboard tracking market cap and liquidity for NVIDIA, TSMC, and Intel. Built with custom DAX overrides to bypass native multi-trillion dollar formatting bugs and preserve data precision.
# Semiconductor Market Cap & Liquidity Dashboard

This is a financial data project built in Power BI to analyze and compare the market capitalization, stock performance, and trading volumes of NVIDIA, TSMC, and Intel. 

The main goal of this dashboard is to provide a clean, side-by-side comparison of how these three hardware giants stack up against each other in total market value and everyday trading activity.

---

## Dashboard View
![Dashboard View](dashboard.png)

## Dashboard Views
![Main Overview](project%20nvidia%20.png)
![Valuation Deep Dive](project%20nvidia%202.png)
![Volume Analysis](project%20nvidia%203.png)
![Historical Trends](project%20nvidia%204.png)

---

## Key Focus Areas
* *Market Value Comparison:* Clear, high-level KPI cards displaying each company's total valuation side-by-side (NVIDIA at $4.15T, TSMC at $1.02T, and Intel at $0.18T).
* *Trading Volume & Liquidity:* A breakdown of daily trading volumes to show which stock sees the most active market participation.
* *Historical Equity Trends:* Charts tracking long-term stock trajectories, handling historical splits to show valuation growth over the years.

---

## Technical Fixes & Power BI Workarounds
While building this, I ran into a native Power BI limitation when handling trillion-dollar figures:

* *The Rounding Issue:* Default Power BI visual settings automatically round up massive numbers or truncate decimals. This caused presentation errors where a multi-billion dollar company like Intel mistakenly rounded all the way down to an incorrect "$0T". 
* *The Fix:* I fixed this by applying a custom format string ($#,##0.00"T") directly to the underlying fields and setting the visual Callout Values to Display Units: None. This forced the dashboard to show exact numbers down to two decimal places without breaking the layout.
* *Data Modeling:* Structured the financial data to handle clean comparisons across different eras of stock history without any performance lag.

---
Built by Mazen.
