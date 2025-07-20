# 🧠 Project Astra - Backend (FastAPI + Gemini Live API)

This is the **backend WebSocket server** for the [Project Astra Flutter Clone](https://github.com/AdnanKhan45/project-astra-flutter), built with **FastAPI** and powered by **Gemini Live API (2.5 Flash)**.  
It acts as the real-time bridge between the user's microphone (from the Flutter app) and Google's Gemini model for streaming audio input and output.

---

## 🔧 What This Backend Does

- Accepts a WebSocket connection from the Flutter client (`/ws/live`)
- Streams **raw microphone audio** to Gemini in real-time
- Receives **AI-generated audio** and subtitles back from Gemini
- Supports control messages like `audio_stream_end` or image input (future-ready)
- Uses `Gemini 2.5 Flash` model with **bidirectional audio** setup and voice transcription

---

## ▶️ How to Run Locally

### 1. **Clone the Repository**
```bash
git clone https://github.com/AdnanKhan45/project-astra-backend.git
cd project-astra-backend
```

### 2. **Install Dependencies**
```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

### 3. **Set Your API Key**
Create a .env file and add your Gemini API key:
```bash
GOOGLE_API_KEY=your-api-key-here
```

### 4. **Run the Server**
```bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

Your WebSocket will now be available at: `wss://localhost:8000/ws/live` or in mobile `wss://your-local-network-ip:8000/ws/live`

### 🤖 Related Project
To test this backend, run the Flutter frontend in [Project Astra](https://github.com/AdnanKhan45/project-astra-flutter) - Flutter Clone. It connects to this backend and brings Astra-style voice interaction to life!

A video on this topic to understand full backend and frontend and its result in action is coming on [eTechViral](https://www.youtube.com/@ETechViral) subscribe and hit the bell icon to stay tuned.

If you found this helpful ⭐️ the repository :) 

