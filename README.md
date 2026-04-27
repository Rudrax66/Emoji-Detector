😂 Emoji Meme Reactor — Computer Vision
A real-time meme reaction app built with Python, OpenCV, and MediaPipe. It detects your hand gestures and facial expressions through your webcam and overlays a matching meme on screen!

📸 How It Works
The app uses your webcam to:

Detect hand gestures via MediaPipe Hands
Detect facial expressions via MediaPipe FaceMesh
Overlay a matching meme image in real time


🛠️ Requirements

Python 3.8 – 3.11 (MediaPipe does not fully support 3.12+)
A working webcam
Good lighting for best detection


📦 Installation
1. Clone or download the project
bashgit clone https://github.com/yourusername/emoji-reactor.git
cd emoji-reactor
2. Create a virtual environment
powershellpython -m venv emoji_env
emoji_env\Scripts\activate
3. Install dependencies
powershellpip install -r requirements.txt

📁 Project Structure
Emoji PY/
│
├── emoji_reactor__1_.py     # Main app file
├── requirements.txt         # Python dependencies
├── README.md                # This file
└── memes/                   # Meme images folder
    ├── ok.jpeg
    ├── air.jpg
    ├── SmiLe copy.jpg
    ├── PlAiN.jpg
    ├── punch.png
    ├── laugh.jpg
    ├── shock.jpg
    ├── thumbs.jpg
    └── peace.jpg

⚠️ The memes/ folder must exist and contain all images listed above, otherwise the app will crash.


▶️ Run the App
powershellpython emoji_reactor__1_.py
Press Q to quit.

🎮 Gestures & Reactions
Gesture / ExpressionMeme Triggered😊 SmileSmiLe copy.jpg😂 Laugh (mouth open wide, eyes squinted)laugh.jpg😮 Shock (mouth + eyes wide open)shock.jpg😐 Plain / Neutral facePlAiN.jpg👌 OK sign (thumb + index close)ok.jpeg🙌 Hands up (all fingers raised)air.jpg🥊 Punch (fingers folded in)punch.png👍 Thumbs upthumbs.jpg✌️ Peace sign (index + middle up)peace.jpg

📋 Dependencies
opencv-python==4.10.0.84
mediapipe==0.10.9
numpy==1.26.4

🧠 How Detection Works
Hand Gestures are detected first (higher priority). If no hand gesture is found, the app falls back to face expression detection.
Smoothing system — a gesture history queue of 9 frames is used with a 1.2 second cooldown to prevent flickering between memes.

🐛 Troubleshooting
ProblemFixmediapipe has no attribute 'solutions'Run pip install mediapipe==0.10.9 --force-reinstallCould not load memes/ok.jpegMake sure all images are inside a memes/ folderNo module named 'pip'Run python -m ensurepip --upgradeWebcam not openingEnsure no other app is using the webcamHand/face not detectedImprove lighting and keep face/hand clearly visibleMeme not changingHold the gesture steady for ~1.5 seconds

📄 License
This project is open source and free to use for educational purposes.
