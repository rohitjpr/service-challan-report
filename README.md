# Service Challan Report App

Flask based internal web app for Service Challan entry, approval, print, Excel import, and Excel export.

## Features
- Login with roles: admin, maker, checker, viewer
- New service challan entry with multiple item rows
- Challan listing with search and filters
- Pending approval screen
- Challan print format
- Excel import from existing challan register format
- Excel export register
- Audit log
- SQLite database for quick deployment

## Default users
- admin / Admin@12345
- maker1 / Maker@12345
- checker1 / Checker@12345
- viewer1 / Viewer@12345

## Local run
```bash
pip install -r requirements.txt
python app.py
```

## Render deploy
1. Push this folder to GitHub
2. Create new Web Service on Render
3. Build command: `pip install -r requirements.txt`
4. Start command: `gunicorn app:app`
5. Add env var `APP_SECRET_KEY`

## Notes
- Change default passwords after first login.
- For heavy multi-user production use, move from SQLite to PostgreSQL.
