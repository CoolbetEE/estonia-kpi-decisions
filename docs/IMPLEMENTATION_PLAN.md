# Implementation Plan (BI‑Native)

**Goal:** Port the logic in this demo into your existing BI tool without exporting any data.

## Steps
1. **Create Calculated Measures**
   - NGR MTD, Turnover MTD, NDCS MTD, NRCS MTD
   - Efficiency = NGR / Turnover
   - WoW deltas using trailing windows
   - Run‑rate = (NGR MTD / days passed) × days in month

2. **Add a Parameter (Scenario)**
   - Values: 0.9 (Downside), 1.0 (Base), 1.1 (Stretch)
   - Projected NGR = Run‑rate × Scenario

3. **Smart Narrative / Text Tile**
   - Bind measures into a short paragraph highlighting WoW deltas and anomalies

4. **Alerts/Subscriptions**
   - A1–A4 from ALERT_CATALOG.md with daily/weekly cadence

5. **Views**
   - Executive summary (headline + narrative + projection)
   - Campaign ROI scorecard (sorted by NGR/Spend)
   - NDCS cohorts (Week of first deposit → D7/D30 NGR/NDCS)

**Security:** All logic runs inside BI; no new apps or data flows required.
