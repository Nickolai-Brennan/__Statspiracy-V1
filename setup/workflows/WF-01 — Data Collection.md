## Additions to WF-01 — Data Collection

### Supported Data Sources

| Source | Type | Prototype | MVP | Production |
|---|---:|---:|---:|---:|
| CSV Upload | File | Yes | Yes | Yes |
| XLSX / Excel Upload | File | Yes | Yes | Yes |
| Python Data Source Script | Script | Yes | Yes | Yes |
| Python Notebook Output | Notebook | Optional | Yes | Yes |
| API Endpoint | API | Optional | Yes | Yes |
| Database Connection | DB | No | Optional | Yes |

---

## Updated Inputs

- Source definitions:
  - CSV file paths
  - XLSX file paths
  - Python script paths
  - Python notebook export paths
  - API endpoints
  - DB connection specs
- Expected schema or column manifest
- `project_brief.md` from WF-00

---

## Updated Raw Ingestion Rules

### CSV Files
- Store unchanged in:
```text
ingested_raw_data/csv/

XLSX Files

Store original workbook unchanged in:


ingested_raw_data/xlsx/

Extract each worksheet into a raw tabular copy:


ingested_raw_data/xlsx_extracted/

Example:

player_stats.xlsx
  Sheet1 → player_stats__sheet1.csv
  Pitching → player_stats__pitching.csv
  Batting → player_stats__batting.csv

Python Data Source Scripts

Python scripts should be registered as ingestion sources when they:

fetch API data

scrape public data

generate derived raw datasets

transform external data into raw exports


Store scripts in:

data_sources/python/

Store script outputs in:

ingested_raw_data/python_outputs/

Recommended structure:

data_sources/
  python/
    fetch_player_stats.py
    fetch_weather_data.py
    scrape_leaderboards.py

ingested_raw_data/
  python_outputs/
    player_stats_raw.csv
    weather_raw.csv
    leaderboard_raw.csv


---

Updated Step 1 — Source Configuration

Action

Parse and validate all data sources:

CSV files

XLSX files

Python source scripts

API endpoints

DB connections


Additional Checks

Confirm file exists

Confirm XLSX workbook opens

Confirm worksheet names

Confirm Python script has safe execution config

Confirm Python script output target

Confirm no credentials are hardcoded


Output

docs/agent-outputs/orchestrator-agent/source_config.md


---

Updated Step 2 — Raw Ingestion

Action

Ingest raw data by source type.

Output Structure

docs/agent-outputs/data-cleanup-agent/ingested_raw_data/
  csv/
  xlsx/
  xlsx_extracted/
  python_outputs/
  api/
  database_exports/


---

Updated Step 3 — Format & Completeness Check

Additional Validation

XLSX Validation

workbook opens

all expected sheets exist

each sheet has headers

row counts captured per sheet

merged cells flagged

hidden sheets flagged

formulas detected and logged


Python Output Validation

script executed successfully

output file created

output schema detected

row count captured

runtime errors logged

warnings captured



---

Updated source_report.md Format

# Source Report

| Source | Type | Format | Rows | Columns | Status | Notes |
|---|---|---:|---:|---:|---|---|
| player_stats.csv | File | CSV | 10,000 | 12 | PASS | Clean import |
| auction_values.xlsx | File | XLSX | 4,200 | 18 | WARNING | 3 sheets detected |
| fetch_weather_data.py | Script | Python | 1,800 | 9 | PASS | Output created |
| sports_api | API | JSON | Pending | Pending | PENDING | API key required |

## XLSX Sheets
| Workbook | Sheet | Rows | Columns | Status |
|---|---|---:|---:|---|
| auction_values.xlsx | Hitters | 2,000 | 18 | PASS |
| auction_values.xlsx | Pitchers | 2,200 | 16 | PASS |
| auction_values.xlsx | Notes | 20 | 3 | WARNING |

## Python Scripts
| Script | Output | Runtime | Status | Notes |
|---|---|---:|---|---|
| fetch_weather_data.py | weather_raw.csv | 4.2s | PASS | No errors |


---

Updated data_inventory.md Format

# Data Inventory

| File | Source Type | Source | Rows | Columns | Date Range | Notes |
|---|---|---|---:|---:|---|---|
| player_stats.csv | CSV | Local Upload | 10,000 | 12 | 2024-01 → 2024-03 | Raw |
| auction_values__hitters.csv | XLSX Sheet | auction_values.xlsx / Hitters | 2,000 | 18 | 2024 | Extracted |
| weather_raw.csv | Python Script Output | fetch_weather_data.py | 1,800 | 9 | 2024-01 → 2024-03 | Raw output |


---

Updated Error Handling

Scenario	Response

XLSX cannot open	Flag critical failure; skip workbook
XLSX missing expected sheet	Flag warning or failure based on manifest
XLSX formulas detected	Log formulas; preserve original workbook
Python script fails	Log traceback summary; mark source failed
Python output missing	Halt that source; notify orchestrator
Python script contains hardcoded secret	Block execution; escalate to orchestrator



---

Updated Safety Gates

[ ] No secrets in Python source files

[ ] Python scripts run in controlled environment

[ ] Original XLSX files preserved unchanged

[ ] Extracted XLSX sheets stored separately

[ ] Script outputs logged with runtime metadata

[ ] All outputs saved to correct directory
