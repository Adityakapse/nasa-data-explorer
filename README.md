# NASA Data Explorer

A full-stack web application for exploring NASA's public data — browse the Astronomy Picture of the Day, track near-Earth asteroids, and search NASA's official image library.

---

## Project Structure

```
nasa-data-explorer/
├── frontend/          # React application
├── backend/           # Node.js / Express API server
└── README.md
```

---

## Features

- **Astronomy Picture of the Day (APOD)** — Browse NASA's daily featured space image or video, pick any historical date
- **Near-Earth Asteroid Dashboard** — Interactive charts (diameter, hazard status, miss distance, count per day) with a full data table
- **NASA Image Library** — Search NASA's official image library by keyword with pagination and a lightbox viewer

---

## Prerequisites

- Node.js v18+
- npm v9+

---

## Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/nasa-data-explorer.git
cd nasa-data-explorer
```

### 2. Backend setup

```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` folder:

```env
NASA_API_KEY=your_nasa_api_key_here
PORT=8000
```

> Get a free API key at [https://api.nasa.gov](https://api.nasa.gov)

### 3. Frontend setup

```bash
cd ../frontend
npm install
```

---

## Running the Application

You need two terminals — one for the backend, one for the frontend.

### Terminal 1 — Start the backend

```bash
cd backend
npm run dev
```

Backend runs at `http://localhost:8000`

### Terminal 2 — Start the frontend

```bash
cd frontend
npm start
```

Frontend runs at `http://localhost:3000`

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## API Endpoints

All endpoints are prefixed with `/api`.

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/apod?date=YYYY-MM-DD` | Astronomy Picture of the Day |
| GET | `/api/neows?start_date=YYYY-MM-DD&end_date=YYYY-MM-DD` | Near-Earth asteroids (max 7-day range) |
| GET | `/api/image?query=mars&page=1` | Search NASA Image Library |
| GET | `/api/epic?date=YYYY-MM-DD` | EPIC Earth imagery |

---

## Tech Stack

### Frontend
- React 19
- React Router DOM
- Axios
- Recharts (data visualisation)
- Tailwind CSS

### Backend
- Node.js
- Express 5
- Axios
- dotenv

---

## Environment Variables

| Variable | Description |
|----------|-------------|
| `NASA_API_KEY` | Your NASA API key (get one free at api.nasa.gov) |
| `PORT` | Backend server port (default: 8000) |
