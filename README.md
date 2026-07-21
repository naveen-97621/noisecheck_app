# NoiseCheck — Tamil Nadu Noise Intelligence Platform 

NoiseCheck is a full-stack, crowdsourced platform designed to map, track, and analyze environmental noise pollution across Tamil Nadu, India. It combines community-submitted noise readings with official federal data (US DOT NTAD 2020 simulation integration) to create an interactive decibel heatmap.

## Features
* **Interactive Heatmap**: Powered by Maplibre GL, visualizing crowdsourced noise reports across Tamil Nadu.
* **Live Decibel Meter**: Web Audio API integration allowing users to log live ambient noise directly from their microphone.
* **Federal Baseline Comparison**: Integration with US DOT NTAD 2020 Transportation Noise data to compare crowdsourced data against simulated federal noise models.
* **User Authentication**: Secure JWT-based registration and login system with `bcrypt` password hashing.
* **Personal Dashboard**: Users can track their total noise logging impact and view their historical contributions.
* **Time & Day Filters**: Filter the state-wide heatmap by Morning/Afternoon/Evening/Night and Weekdays vs Weekends.

## Tech Stack
* **Frontend**: Vanilla HTML/CSS/JS, Maplibre GL (Maps), Chart.js (Analytics)
* **Backend**: FastAPI (Python), SQLAlchemy (ORM), SQLite (Database)
* **Security**: PyJWT, bcrypt

## How to Run Locally

### 1. Setup the Backend
Navigate to the `backend` directory and install the requirements:
```bash
cd backend
pip install -r requirements.txt
```

### 2. Configure Environment (Optional)
Create a `.env` file in the `backend` directory if you want to override the default JWT Secret:
```env
JWT_SECRET=your-super-secret-key
```

### 3. Run the Server
The FastAPI backend serves both the API and the static frontend assets. Run it using `uvicorn`:
```bash
python -m uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

### 4. Open the App
Navigate to [http://localhost:8000](http://localhost:8000) in your web browser.

## Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

