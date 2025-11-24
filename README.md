# Digital-Storage-Oscilloscope

Digital Modulation Simulator & Virtual Oscilloscope — a full‑stack web app that simulates and visualizes common digital and pulse modulation techniques with a virtual DSO interface (interactive cursors, ΔT, frequency, multi‑channel plotting).

Features
- Modulation techniques: ASK, FSK, PSK (carrier‑based), and pulse modulations: PAM, PWM, PPM.
- Visualizations: digital input (bitstream), carrier, and resulting modulated output.
- Oscilloscope tools: two vertical cursors, ΔTime and derived frequency, Time/Div and Volts/Div display.

Tech stack
- Frontend: React, react-plotly.js (Plotly), Axios
- Backend: Python 3, Flask, NumPy
- Styling: CSS (Grid & Flexbox), dark/scientific UI

Quick setup (Windows)

1) Backend
- Open a terminal and go to the backend folder:
  cd backend
- (Optional) Create and activate venv:
  python -m venv venv
  venv\Scripts\activate
- Install dependencies:
  pip install flask flask-cors numpy
- Start server:
  python app.py
  # by default: http://127.0.0.1:5000

2) Frontend
- In a separate terminal:
  cd frontend
  npm install
  npm start
  # React dev server: http://localhost:3000

How to use
- Select modulation type, enter a binary bitstream (e.g., 10110), set carrier frequency and amplitude, then click Generate Signals.
- Enable cursors to place Cursor 1 and Cursor 2 on the plot; the sidebar LCD shows Δt and frequency (1/Δt).

Project structure (root)
- backend/      — Flask server and signal generation code (app.py)
- frontend/     — React app (src/, package.json)
- README.md

Troubleshooting
- "Network Error": ensure backend is running on port 5000 and frontend on 3000.
- Frontend module not found: run npm install inside frontend.
- Backend module not found: ensure venv activated (if used) and run pip install flask flask-cors numpy.

Notes
- This README focuses on setup and basic usage. See inline comments in backend/app.py and frontend/src/ for implementation details and extension points.
- For reproducible installs, consider adding requirements.txt (backend) and locking frontend dependencies (package-lock.json / pnpm/yarn).