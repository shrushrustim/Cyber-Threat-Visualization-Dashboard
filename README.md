# Cyber-Threat-Visualization-Dashboard

# Modules 1 & 2 — Data Acquisition, Normalization & Core Visualizations

# Project Structure

'cyber-threat-dashboard/
├── config/
│   ├── schema.py          # Pydantic models — ThreatEvent, CVEEvent, GeoLocation
│   ├── settings.py        # All env vars and constants
│   └── database.py        # MongoDB connection + all query helpers
│
├── ingestion/
│   ├── fetch_nvd.py        # Module 1 — NVD CVE feed (free, no key needed)
│   ├── fetch_otx.py        # Module 1 — AlienVault OTX threat pulses
│   ├── fetch_abuseipdb.py  # Module 1 — AbuseIPDB blacklist + GeoIP enrichment
│   ├── simulate_data.py    # Realistic simulated data (for dev/demo)
│   └── fetch_all.py        # Master orchestrator — runs all sources
│
├── visualizations/
│   ├── charts.py           # Module 2 — Time-series, bar, donut, heatmap
│   └── geo_charts.py       # Module 3 — Choropleth, scatter geo, treemap, sunburst
│
├── dashboard/
│   └── app.py              # Module 4 — Full Plotly/Dash dashboard
│
├── .github/workflows/
│   └── ingest.yml          # Free GitHub Actions cron (every 15 min)
│
├── requirements.txt
├── .env.example
└── README.md'
