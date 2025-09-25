# Mood Music Project

This project is a web application that suggests music based on your current mood. It uses a React frontend to capture your mood and a Node.js backend to communicate with the Spotify and Gemini APIs to generate a relevant playlist.

## Technology Stack

- **Frontend:** React, Vite, Tailwind CSS
- **Backend:** Node.js, Express.js
- **APIs:** Spotify API, Google Gemini API
- **Package Manager:** pnpm

## Features Implemented

- Mood-based music recommendations.
- Dynamic keyword generation for playlist searching using Google Gemini.
- Fetches and displays a list of tracks from Spotify.
- Randomizes the track order for a fresh playlist every time.
- Simple, clean user interface.

## Demo

You can view a live demo of the project here: [mic-frontend.a2ys.dev](https://mic-frontend.a2ys.dev)

## How to Get Started

To get this project running on your local machine, you'll need to set up both the backend and the frontend. Make sure you have Node.js and pnpm installed before you begin.

### Backend Setup

The backend is responsible for handling API requests to Spotify and Google's Gemini.

1. **Navigate to the backend directory:**

   ```sh
   cd backend
   ```

2. **Install dependencies:**
   Run the following command to install the necessary packages.

   ```sh
   pnpm install
   ```

3. **Set up environment variables:**
   Create a new file named `.env` in the `backend` folder. This file will store your API keys and other configuration details. Add the following variables to it:

   ```env
   SPOTIFY_CLIENT_ID="your_spotify_client_id"
   SPOTIFY_CLIENT_SECRET="your_spotify_client_secret"
   GEMINI_API_KEY="your_gemini_api_key"
   PORT=5000
   ```

   You can obtain the Spotify keys from the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/) and the Gemini key from the [Google AI Studio](https://aistudio.google.com/app/apikey).

4. **Run the backend server:**

   ```sh
   pnpm start
   ```

   The server will start and listen for requests on `http://localhost:5000`.

### Frontend Setup

The frontend is a React application that provides the user interface.

1. **Navigate to the frontend directory:**
   In a new terminal, change to the frontend directory.

   ```sh
   cd frontend
   ```

2. **Install dependencies:**
   Install the required packages for the frontend.

   ```sh
   pnpm install
   ```

3. **Create a `.env` file:**
   Create a `.env` file in the `frontend` directory and add the following line to specify the backend server URL:

   ```env
   VITE_BACKEND_URL=http://localhost:5000
   ```

4. **Run the frontend application:**

   ```sh
   pnpm dev
   ```

   This command will start the development server, and you can view the application by navigating to the URL provided in the terminal (usually `http://localhost:5173`).

Once both the backend and frontend are running, you can use the application to get music recommendations based on your mood.
