# Cyber-Threat-Visualization-Dashboard

# Modules 1 & 2 — Data Acquisition, Normalization & Core Visualizations

# Project Structure

```bash
cyber-threat-dashboard/
├── config/
│   ├── schema.py        # Pydantic models – ThreatEvent, CVEEvent, GeoLocation
│   ├── settings.py      # All env vars and constants
│   └── database.py      # MongoDB connection + all query helpers
│
├── ingestion/
│   ├── fetch_nvd.py         # Module 1 – NVD CVE feed
│   ├── fetch_otx.py         # Module 1 – AlienVault OTX
│   ├── fetch_abuseipdb.py   # Module 1 – AbuseIPDB + GeoIP
│   ├── simulate_data.py     # Simulated data (dev/demo)
│   └── fetch_all.py         # Master orchestrator
│
├── visualizations/
│   ├── charts.py        # Module 2 – Charts
│   └── geo_charts.py    # Module 3 – Geo charts
│
├── dashboard/
│   └── app.py           # Module 4 – Dashboard
│
├── .github/workflows/
│   └── ingest.yml       # GitHub Actions
│
├── requirements.txt
├── .env.example
└── README.md
```
