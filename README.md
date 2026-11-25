# City Pulse

# End-to-end Data Pipeline Combining Crime Data From Major Cities into One Uniform Source

## Source notes: NYC
- Current year: https://data.cityofnewyork.us/d/5uac-w243 (2026 YTD, ~427k rows)
- Historic: https://data.cityofnewyork.us/d/qgea-i56i (2006–2025, ~10M rows)
- Split by report date: historic ends 2025-12-31, current starts 2026-01-01
- API v2 `/resource/<id>.json`: default 1,000 rows/request, needs paging
- API v3: needs app token, ignores `$limit` without one
- All fields come back as text
- API flaky sometimes (retry)
- Bad dates (year 1010), ~2% of reports are for older crimes