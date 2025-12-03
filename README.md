# RuDwaar OS — Prototype
A minimal open-source prototype for the "RuDwaar OS" hackathon entry.
This repo contains a lightweight Flask backend, sample data, tests, architecture docs, and setup instructions.

## Contents
- `backend/` — Flask API implementing core endpoints (advisory, marketplace, jobs, schemes stub)
- `sample_data/` — sample JSON/CSV data for demos
- `tests/` — pytest tests for the API
- `architecture.md` — architecture and design notes
- `LICENSE` — MIT License
- `requirements.txt` — Python dependencies

## Quick start (Linux / macOS)
1. Clone or download this repository.
2. Create virtualenv:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the API:
   ```bash
   cd backend
   export FLASK_APP=app.py
   flask run --host=0.0.0.0 --port=5000
   ```
5. API endpoints:
   - `GET /health` — health check
   - `POST /advisory` — body: `{ "crop": "wheat", "location": "villageX", "image": null }`
   - `GET /marketplace` — list produce
   - `POST /jobs` — post a job
   - `GET /schemes?profile_type=farmer` — list relevant schemes (stub)
6. Run tests:
   ```bash
   pytest -q
   ```

## License
MIT — see `LICENSE`.

## Notes
This is a hackathon prototype to demonstrate architecture and core flows. It is intentionally minimal and suitable for extension.
