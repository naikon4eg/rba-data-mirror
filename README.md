# RBA A1 data mirror

This repository is a transport mirror for the unchanged official Reserve Bank of Australia A1 CSV:

- Official source: `https://www.rba.gov.au/statistics/tables/csv/a1-data.csv`
- Mirrored file: `data/a1-data.csv`
- Required RBA series: `ARBAATAW` — Total assets

The GitHub Action runs daily and can also be started manually from **Actions → Update RBA A1 mirror → Run workflow**.

## Required repository name

The supplied n8n workflow is preconfigured for:

- GitHub owner: `naikon4eg`
- Repository: `rba-data-mirror`
- Branch: `main`

Resulting Raw URL:

`https://raw.githubusercontent.com/naikon4eg/rba-data-mirror/main/data/a1-data.csv`

If the owner, repository, branch, or path differs, edit the constants at the beginning of the n8n node **RBA Request Registry**.

## Setup

1. Create a **public** GitHub repository named `rba-data-mirror`.
2. Upload this package preserving the `.github/workflows` and `data` directories.
3. Open the repository's **Actions** tab and enable workflows if GitHub asks.
4. Run **Update RBA A1 mirror** manually once.
5. Confirm that `data/a1-data.csv` exists and contains `ARBAATAW`.
6. Import the supplied full n8n workflow JSON and run it.

GitHub is used only as a delivery layer. Source attribution inside the report remains the official RBA URL.
