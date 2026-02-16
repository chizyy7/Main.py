# Main.py/penalty shootout game
A simple python game project for practice and learning

⚽ Penalty Shootout Game (Kivy + Python + Android)

📱 Overview

Penalty Shootout is a mobile football penalty game built using Python and the Kivy framework, then packaged into an Android app using Buildozer and Python-for-Android.

The game simulates a penalty shootout scenario where the player shoots a ball toward goal while a goalkeeper attempts to save it. The project demonstrates cross-platform Python game development and Android deployment without using Java or Kotlin.

⸻

🎮 Features
	•	Animated football and goalkeeper
	•	Goal detection system
	•	Save detection logic
	•	Sound effects (kick, goal, save)
	•	Start screen with difficulty selection
	•	Score tracking
	•	Mobile-friendly layout
	•	Android APK build

⸻

🛠️ Technologies Used
	•	Python 3
	•	Kivy
	•	Buildozer
	•	Python-for-Android
	•	SDL2
	•	WSL (Ubuntu on Windows)

⸻

📂 Project Structure

penaltyshootoutGame/
│
├── assets/
│   ├── images/
│   │   ├── background.png
│   │   ├── ball.png
│   │   ├── goal.png
│   │   └── keeper.png
│   │
│   └── sounds/
│       ├── kick.wav
│       ├── goal.wav
│       └── save.wav
│
├── main.py
├── buildozer.spec
├── bin/
└── README.md

🧠 Game Logic Explanation

Ball Shooting

When the player taps the screen, the ball animates toward a random target position inside the goal area using Kivy Animation.

Goalkeeper Movement

The goalkeeper moves randomly left or right based on difficulty level and timing.

Collision Detection

The game checks whether:
	•	Ball overlaps goalkeeper → Save
	•	Ball enters goal area → Goal

Sound System

Sounds are loaded using:

from kivy.core.audio import SoundLoader:

self.kick_sound = SoundLoader.load("assets/sounds/kick.wav")
self.goal_sound = SoundLoader.load("assets/sounds/goal.wav")
self.save_sound = SoundLoader.load("assets/sounds/save.wav")

And played during events:

self.kick_sound.play()
self.goal_sound.play()
self.save_sound.play()

🚀 Development Process

This project went through multiple real-world stages:

1️⃣ Desktop Game Prototype

The game was first built and tested locally on Ubuntu using:
python main.py

This allowed testing of:
	•	Animations
	•	Layout
	•	Game logic
	•	Sound triggers

⸻

2️⃣ Asset Integration

Images and sounds were added into structured folders:
assets/images
assets/sounds

Paths were referenced in code to ensure Android compatibility.

⸻

3️⃣ Android Packaging Setup

Android build environment created using:
buildozer init

Then configuration edited in:
buldozer.spec

Key settings:

requirements = python3,kivy
orientation = portrait
fullscreen = 1
android.permissions = INTERNET

4️⃣ APK Build

Android APK compiled with:
buildozer andriod debug

Output APK:
bin/penaltyshootout-0.1-debug.apk
⸻

5️⃣ Device Testing

APK transferred to Android phone and installed manually.

Testing revealed issues including:
	•	Missing assets
	•	Indentation errors
	•	Python library loading
	•	Sound playback
	•	SDL rendering crashes

These were debugged using:
adb logcat

6️⃣ Debugging Challenges Solved

During development, several real Android deployment issues were fixed:
	•	Python indentation errors
	•	Asset path resolution
	•	Sound loading problems
	•	SDL crash on launch
	•	Kivy packaging issues
	•	WSL file access
	•	Buildozer configuration

This reflects real mobile game development troubleshooting.

⸻

📦 How to Run (Desktop)
Install dependencies:
pip install kivy

Run game:
python main.py

📱 How to Build Android APK

Inside project folder:
buildozer andriod debug

APK will appear in:
bin/
install on phone and run.

🎯 Learning Outcomes

This project demonstrates:
	•	Python game development
	•	Kivy UI and animation
	•	Mobile deployment with Buildozer
	•	Android packaging without Java
	•	Debugging native crashes
	•	Asset management in apps
	•	Cross-platform development workflow

⸻

🔮 Future Improvements

Planned features:
	•	Multiple difficulty levels
	•	Scoreboard persistence
	•	Better goalkeeper AI
	•	Sound settings
	•	Ad integration
	•	Google Play release
	•	Improved UI design
	•	Goal celebration animation

⸻

🙌 Author

Chizy

Aspiring software developer focused on:
	•	Game development
	•	Mobile apps
	•	Web development
	•	AI tools

⸻

⭐ Acknowledgment

This project was built as part of a personal learning journey into Python game development and Android deployment using Kivy and Buildozer.
