# India-Stocks-2221-2250-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2221 to 2250)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2221-2250-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2221 to 2250)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2221 | `ARHAM` | Arham Technologies Limited | `ARHAM.NS` |
| 2222 | `SINGERIND` | Singer India Limited | `SINGERIND.NS` |
| 2223 | `SINTERCOM` | Sintercom India Limited | `SINTERCOM.NS` |
| 2224 | `SIRCA` | Sirca Paints India Limited | `SIRCA.NS` |
| 2225 | `SIS` | SIS LIMITED | `SIS.NS` |
| 2226 | `SITINET` | Siti Networks Limited | `SITINET.NS` |
| 2227 | `SIYSIL` | Siyaram Silk Mills Limited | `SIYSIL.NS` |
| 2228 | `SJS` | S.J.S. Enterprises Limited | `SJS.NS` |
| 2229 | `SKFINDIA` | SKF India Limited | `SKFINDIA.NS` |
| 2230 | `SKFINDUS` | SKF India (Industrial) Limited | `SKFINDUS.NS` |
| 2231 | `SKIPPER` | Skipper Limited | `SKIPPER.NS` |
| 2232 | `SKMEGGPROD` | SKM Egg Products Export (India) Limited | `SKMEGGPROD.NS` |
| 2233 | `SKYGOLD` | SKY GOLD AND DIAMONDS LIMITED | `SKYGOLD.NS` |
| 2234 | `SKYWAYS` | Skyways Air Services Limited | `SKYWAYS.NS` |
| 2235 | `SMARTLINK` | Smartlink Holdings Limited | `SMARTLINK.NS` |
| 2236 | `SMARTWORKS` | Smartworks Coworking Spaces Limited | `SMARTWORKS.NS` |
| 2237 | `SMCGLOBAL` | SMC Global Securities Limited | `SMCGLOBAL.NS` |
| 2238 | `SMLMAH` | SML Mahindra Limited | `SMLMAH.NS` |
| 2239 | `SMLT` | Sarthak Metals Limited | `SMLT.NS` |
| 2240 | `SMSPHARMA` | SMS Pharmaceuticals Limited | `SMSPHARMA.NS` |
| 2241 | `SMT` | Sahajanand Medical Technologies Limited | `SMT.NS` |
| 2242 | `SNOWMAN` | Snowman Logistics Limited | `SNOWMAN.NS` |
| 2243 | `SOFTTECH` | Softtech Engineers Limited | `SOFTTECH.NS` |
| 2244 | `SOLARA` | Solara Active Pharma Sciences Limited | `SOLARA.NS` |
| 2245 | `SOLARWORLD` | Solarworld Energy Solutions Limited | `SOLARWORLD.NS` |
| 2246 | `SOLEX` | Solex Energy Limited | `SOLEX.NS` |
| 2247 | `SOMANYCERA` | Somany Ceramics Limited | `SOMANYCERA.NS` |
| 2248 | `SOMATEX` | Soma Textiles & Industries Limited | `SOMATEX.NS` |
| 2249 | `SOMICONVEY` | Somi Conveyor Beltings Limited | `SOMICONVEY.NS` |
| 2250 | `SONA` | Sonaselection India Limited | `SONA.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream ARHAM 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2221-2250-Historical-Data/main/ARHAM/1m/2026/10/ARHAM_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
