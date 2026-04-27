# 🏓 PONG — Hand Controlled (Computer Vision)

A real-time hand-controlled Pong game built with Python, OpenCV, MediaPipe, and Pygame. Control the paddles using your hands in front of a webcam — no keyboard or mouse needed!

---

## 📸 How It Works

The game uses your webcam to detect hand positions via **MediaPipe**. Your **index fingertip** controls the paddle height in real time.

- **Left hand** → controls **Player 1** (left paddle)
- **Right hand** → controls **Player 2** (right paddle)

---

## 🛠️ Requirements

- Python **3.8 – 3.11** (MediaPipe does not fully support 3.12+)
- A working **webcam**
- Good **lighting** for hand detection

---

## 📦 Installation

### 1. Clone or download the project

```bash
git clone https://github.com/yourusername/pong_cv.git
cd pong_cv
```

### 2. Create a virtual environment

```powershell
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Game

```bash
python pong_cv.py
```

---

## 🎮 Controls

| Action              | Input                        |
|---------------------|------------------------------|
| Move P1 paddle      | Raise/lower your **left hand**  |
| Move P2 paddle      | Raise/lower your **right hand** |
| Quit game           | Press `Q` or `Esc`           |
| Restart after win   | Press `R`                    |

---

## 📁 Project Structure

```
pong_cv/
│
├── pong_cv.py          # Main game file (hand-controlled Pong)
├── pythongame.py       # Bonus: Word guessing game (tkinter)
├── requirements.txt    # Python dependencies
└── README.md           # This file
```

---

## 📋 Dependencies

```
pygame==2.6.1
opencv-python==4.10.0.84
mediapipe==0.10.9
```

> `tkinter` is built into Python — no install needed for `pythongame.py`.

---

## 🧠 Game Rules

- First player to score **4 points** wins
- The ball speeds up slightly with each paddle hit (max speed capped)
- The angle of the ball changes based on where it hits the paddle
- If no hand is detected, the paddle stays in its last position

---

## 🐛 Troubleshooting

| Problem | Fix |
|---|---|
| `No module named 'pip'` | Run `python -m ensurepip --upgrade` |
| `mediapipe has no attribute 'solutions'` | Run `pip install mediapipe==0.10.9` |
| Webcam not detected | Check webcam is connected and not used by another app |
| Hand not detected | Improve lighting; keep hand fully visible in frame |
| Black screen | Ensure your webcam drivers are up to date |

---

## 🪀 Bonus Game — Word Guesser

A simple tkinter-based word guessing game is also included.

```bash
python pythongame.py
```

- A random word is displayed as blanks (`_ _ _ _`)
- Type one letter at a time and click **Guess**
- You have **5 lives** — wrong guesses reduce lives
- Guess the full word before running out!

---

## 📄 License

This project is open source and free to use for educational purposes.
