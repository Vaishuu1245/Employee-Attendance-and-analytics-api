# Employee Attendance & Analytics API

A Python + FastAPI + MongoDB starter for the HROne Software Engineer Trainee assignment.

## Requirements
- Python 3.11+
- MongoDB 6.0+
- Git

## Setup (Windows PowerShell)

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
$env:MONGODB_URI = "mongodb://localhost:27017"
$env:DATABASE_NAME = "employee_attendance"
uvicorn app.main:app --reload
```

If PowerShell blocks activation, use Command Prompt:
```bat
.venv\Scripts\activate.bat
```

## Run
Open:
- API health: http://127.0.0.1:8000/health
- MongoDB health: http://127.0.0.1:8000/health/database
- Swagger UI: http://127.0.0.1:8000/docs

## Before submission
1. Read the official problem statement, OpenAPI contract, data model, sample data, and starter app from the assignment kit.
2. Implement every required endpoint and exact business rule.
3. Use MongoDB aggregation pipelines for the required analytics endpoints.
4. Complete `REVIEW.md` and `DECISIONS.md` based on the supplied files and your actual implementation.
5. Add tests and run them.
6. Do not commit `.env` files, passwords, tokens, or other secrets.
7. This is a starter scaffold; it is not a complete assignment yet.

## Known missing work
- Official attendance endpoints and request/response schemas
- Punch-in/punch-out business rules
- Manual correction and audit history
- Required aggregation analytics
- Code review of the supplied existing code
- Design decisions based on the official specification
- Automated tests
