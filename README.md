# LeadAtlas — Responsible B2B Lead Research

This repository is reserved for the LeadAtlas FastAPI + Streamlit + SQLite application.

**Project source:** The full runnable project ZIP was delivered in the ChatGPT conversation where this repository was connected. Extract `ai-b2b-lead-agent.zip` and upload its contents to the repository to publish the complete code.

## Local run

```bash
python -m venv .venv
# Activate the virtual environment
pip install -r requirements.txt
uvicorn app.api:app --port 8000
# In another terminal
streamlit run dashboard.py
```

Dashboard: http://localhost:8501 · API docs: http://localhost:8000/docs

Alternative: `docker compose up --build`.

## Design

- Source-bound company research from OpenStreetMap/Overpass, up to 20 records per run
- India, USA, UK and UAE; country/industry/size filtering
- Public business contact data only; unknowns remain unknown
- Robots-aware, public HTTPS homepage audits
- Explainable rule-based lead scoring and grounded outreach templates
- Manual approval; no automated email sending
- CSV export, synthetic demo mode, pytest tests and Docker configuration

**Caveats:** This initial version has rules-based scoring and templates, not an integrated LLM. Production use requires stronger authentication, network safeguards and applicable privacy/marketing compliance. OpenStreetMap © OpenStreetMap contributors, ODbL; https://www.openstreetmap.org/copyright.
