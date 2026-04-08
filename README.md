# SAN Commissioning Dashboard

Commissioning progress dashboard for San Diego International Airport (SAN) projects. Built on the CriticalArc dashboard template, pulling real-time data from the CxAlloy API.

---

## Overview

This dashboard tracks commissioning activities across SAN airport projects, providing visibility into issues, checklists, functional tests, and equipment status. Project managers and commissioning agents can monitor progress, identify bottlenecks, and track contractor performance through a single interface.

### Dashboard Tabs

- **Issue Tracking** — Open issues, aging reports, priority breakdowns, issues by division and contractor
- **Checklist (PFC)** — Pre-functional checklist pipeline, completion by discipline and contractor, pending assignments
- **Functional Tests** — Test pass rates, attempt tracking, tests by division and equipment type
- **Equipment** — Equipment inventory with linked checklists/tests/issues, filterable by floor and space

---

## Setup

See the [template README](https://github.com/kspann-hub/criticalarc-dashboard) for full setup instructions. Quick start:

1. Clone this repo
2. Create venv and `pip install -r requirements.txt`
3. Add CxAlloy credentials to `.streamlit/secrets.toml`
4. Run `python inspect_data.py` to verify data
5. Run `streamlit run app.py`

---

## Security

- **Never commit `.streamlit/secrets.toml`** — it is excluded via `.gitignore`
- API credentials belong only in your local `secrets.toml` and Streamlit Cloud's Advanced Settings
- If secrets are accidentally committed, rotate your CxAlloy API key immediately