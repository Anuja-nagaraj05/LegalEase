# LegalEase - AI Legal Document Generator

## Setup
1. `python -m venv venv` then activate it (`venv\Scripts\activate` on Windows)
2. `pip install -r requirements.txt`
3. Copy `.env.example` to `.env` and add your Gemini API key (https://aistudio.google.com/apikey)
4. Optional: put your logo at `Image/Logo.png`

## Run (two terminals, from the project root)
    uvicorn legalEaseAPI.main:app --reload
    streamlit run frontend/app.py

Open http://localhost:8501. The API docs are at http://localhost:8000/docs.

## Sample input
- Type: Freelance Work Contract
- Parties: Jane Doe (Service Provider), TechNova Inc. (Client)
- Terms: Work delivered by May 15, 2025; Payment within 7 days of invoice; Client retains IP rights
- Date: April 15, 2025

## Deploy
Backend (Render/Railway/Fly.io): `uvicorn legalEaseAPI.main:app --host 0.0.0.0 --port $PORT`
Frontend (Streamlit Community Cloud): set `BACKEND_URL` to your deployed backend URL.
