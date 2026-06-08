# 🍉 Hand Tracking Fruit Slicer

<div align="center">

A **Fruit Ninja**-style browser game powered by **MediaPipe hand tracking** — slice fruits with your bare hands using just a webcam. No controllers needed.

![Game](https://img.shields.io/badge/Game-Fruit%20Slicer-red)
![Tech](https://img.shields.io/badge/Tech-MediaPipe%20%7C%20Canvas%20%7C%20Tailwind-blue)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

---

## ✨ Features

- **Hand Tracking Mode** — Play using your webcam with real-time MediaPipe hand landmark detection
- **Mouse Mode** — Play without a camera using mouse/touch input
- **Real-time Slicing** — Smooth swipe-to-slice mechanics with trail rendering
- **Audio Feedback** — Procedural sound effects for slicing, misses, and game events
- **HUD System** — Score, timer, lives (❤️❤️❤️), FPS counter, and tracking status
- **Responsive Design** — Full-screen canvas that adapts to any display size

---

## 🎮 How to Play

1. **Start the game** — Choose "Play with Camera" or "Play without Camera (Mouse)"
2. **Slice fruits** — Swipe through fruits to slice them
3. **Avoid bombs** — Don't slice the bombs or you'll lose a life
4. **Survive** — Don't let fruits fall off screen or you lose lives
5. **Beat your high score** — Keep playing to top your best score

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| **HTML5 Canvas** | Game rendering engine |
| **MediaPipe Hands** | Real-time hand landmark detection |
| **Tailwind CSS v4** | UI styling and layout |
| **Vite** | Build tool and dev server |
| **TypeScript** | Type-safe game logic |
| **Web Audio API** | Procedural sound effects |

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- A webcam (for hand tracking mode)
- Modern browser with WebGL support

### Installation

```bash
git clone https://github.com/karthikeyagoud045-ANU/hand-gesture-fruit-slicing-game.git
cd hand-gesture-fruit-slicing-game
npm install
```

### Run Locally

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build for Production

```bash
npm run build
npm run preview
```

---

## 📁 Project Structure

```
hand-gesture-fruit-slicing-game/
├── index.html          # Main game HTML + Canvas + MediaPipe integration
├── src/
│   ├── App.tsx         # React app shell
│   ├── main.tsx        # React entry point
│   └── index.css       # Tailwind imports
├── package.json        # Dependencies and scripts
├── vite.config.ts      # Vite configuration
├── tsconfig.json       # TypeScript configuration
└── .env.example        # Environment variable template
```

---

## 🔧 Configuration

| Variable | Description | Required |
|---|---|---|
| `GEMINI_API_KEY` | Google Gemini API key (for AI features) | Optional |
| `APP_URL` | App URL for self-referential links | Auto-injected |

---

## 🧠 How Hand Tracking Works

1. **MediaPipe Hands** detects 21 hand landmarks in real-time from the webcam feed
2. The **index finger tip (landmark 8)** is used as the primary tracking point
3. Coordinates are mapped from video space to canvas space
4. A **swipe trail** is rendered behind the finger movement
5. **Collision detection** checks if the trail intersects with fruit objects

---

## 📝 License

MIT License — feel free to use, modify, and distribute.
