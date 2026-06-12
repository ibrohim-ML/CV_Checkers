<p align="center">
  <img src="https://img.shields.io/badge/status-active-success" alt="Status">
  <img src="https://img.shields.io/badge/checkers-⛊-white?labelColor=black" alt="Checkers">
  <img src="https://img.shields.io/badge/MediaPipe-Hands-blue" alt="MediaPipe">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License">
</p>

<br>

<p align="center">
  <strong>⛊ CV Checkers ⛊</strong><br>
  <em>Touchless. Intuitive. Checkers.</em>
</p>

<p align="center">
  Control the checkers board with nothing but your hand — <br>
  no mouse, no keyboard, no touchscreen. Just you and the camera.
</p>

<br>

---

# CV Checkers

> **Camera-controlled checkers game using real-time hand tracking**

CV Checkers is a browser-based checkers (draughts) game that uses **MediaPipe Hands** to track your fingers in real time. Point at pieces, pinch to grab, release to move — all without touching a thing.

---

## ✨ Features

- **Hand tracking** — index finger controls the cursor; pinch with thumb to grab
- **Full checkers rules** — mandatory captures, king promotion, multi-jump
- **King pieces** — crowned pieces move and capture backward
- **Real-time feedback** — on-screen cursor, debug panel, and status indicators
- **Smooth cursor** — adaptive smoothing for natural hand movement
- **Responsive** — works on desktop and tablet browsers
- **No dependencies** — pure HTML, CSS, and JavaScript

---

## 🎮 How It Works

| Action | Gesture |
|--------|---------|
| Move cursor | Move your index finger |
| Grab a piece | Pinch (bring thumb and index together) |
| Release / move | Open your hand |

The camera feed is processed entirely in the browser via **MediaPipe**. Your hand landmarks are mapped to board coordinates, and a hysteresis-based pinch detector ensures stable grab/release transitions.

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| Hand tracking | [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) |
| Rendering | HTML5 Canvas + CSS Grid |
| Camera | MediaPipe Camera Utils |
| Logic | Vanilla JavaScript (ES6) |

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/ibrohim-ML/CV_Checkers.git
cd CV_Checkers

# Start a local server
python -m http.server 8000
```

Open **http://localhost:8000** in your browser and click **"Kamerani yoqish"** to begin.

> **Note:** Camera access requires **localhost** or **HTTPS**. Use the local server above — do not open the file directly (`file://`).

---

## 📁 Project Structure

```
CV_Checkers/
├── index.html      # All game logic, styles, and markup
├── README.md       # This file
└── .gitignore
```

Everything is in a single HTML file — no build tools, no bundlers, no frameworks.

---

## 🧠 Architecture

The game runs a fixed-timestep animation loop (`requestAnimationFrame`) that:

1. Reads the latest hand landmarks from MediaPipe
2. Maps normalized coordinates to board-local pixel space
3. Applies adaptive smoothing for jitter reduction
4. Detects pinch state with hysteresis (ON at < 0.035, OFF at > 0.050)
5. Computes legal moves including mandatory captures and multi-jumps
6. Renders the board, cursor, drag ghost, and UI overlays

---

## 📄 License

This project is licensed under the **MIT License**.

---

<br>

<h1 align="center">⛊ CV Checkers ⛊</h1>
<p align="center"><em>Sensorlarsiz. Intuitiv. Shashka.</em></p>
<p align="center">Shashka taxtasini faqat qo'lingiz bilan boshqaring —<br>sichqoncha, klaviatura yoki sensor kerak emas. Faqat siz va kamera.</p>

---

## CV Checkers

> **Real vaqt rejimida qo'l tracking orqali boshqariladigan veb-shashka**

CV Checkers — bu **MediaPipe Hands** yordamida barmoqlaringizni real vaqtda kuzatib, shashka o'ynash imkonini beruvchi brauzer ilovasi.

---

## ✨ Xususiyatlar

- **Qo'l tracking** — ko'rsatkich barmoq kursor vazifasini bajaradi; chimchish bilan ushlash
- **To'liq shashka qoidalari** — majburiy urish, damka bo'lish, ko'p marta urish
- **Damkalar** — toj kiydirilgan damkalar orqaga ham yura oladi
- **Silliq kursor** — moslashuvchan tekislash tabiiy harakat uchun
- **Hech qanday kutubxona kerak emas** — sof HTML, CSS va JavaScript

---

## 🎮 Qanday ishlaydi

| Harakat | Imo-ishora |
|---------|------------|
| Kursorni harakatlantirish | Ko'rsatkich barmoqni siljitish |
| Shashkani ushlash | Chimchish (bosh va ko'rsatkich barmoqni birlashtirish) |
| Qo'yib yuborish / yurish | Qo'lni ochish |

---

## 🧰 Texnologiyalar

| Qatlam | Texnologiya |
|--------|-------------|
| Qo'l tracking | [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) |
| Chizish | HTML5 Canvas + CSS Grid |
| Kamera | MediaPipe Camera Utils |
| Logika | Sof JavaScript (ES6) |

---

## 🚀 Ishga tushirish

```bash
git clone https://github.com/ibrohim-ML/CV_Checkers.git
cd CV_Checkers
python -m http.server 8000
```

Brauzerda **http://localhost:8000** ni oching.

---

## 📄 Litsenziya

MIT
