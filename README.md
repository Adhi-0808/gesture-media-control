Gesture Media Control System

Project Overview
This project implements a real-time hand gesture-based media control system for Linux using computer vision.

The system uses a webcam and detects hand gestures to control:
Play / Pause
Next / Previous track
Seek forward/backward
Volume (Analog pinch control)
Mute
Fullscreen
Audio & Subtitle switching
It provides a touchless human-computer interaction system optimized for Linux media players.

video demo link:
https://drive.google.com/file/d/1ZpYDixzAgNZ4VRF0OS7tAIKCGaJ2tYLD/view?usp=sharing

Core Concept
The system uses:
MediaPipe Hands for real-time hand landmark detection
OpenCV for video capture and display
pactl for Linux volume control
playerctl for media control
xdotool for keyboard simulation

Gesture Mapping
Static Gestures
Gesture	Action
Open Palm (5 fingers)	Play
Fist (0 fingers)	Pause
Two Fingers	Mute
Thumb + Little Finger	Fullscreen
Pinch Control (Thumb + Index Close)
Movement	Action
Move Right	Next Track
Move Left	Previous Track
Move Up	Increase Volume (Analog)
Move Down	Decrease Volume (Analog)
Swipe Gestures
Fingers	Swipe	Action
1 Finger	Left/Right	Seek -10s / +10s
3 Fingers	Left/Right	Subtitle Prev/Next
4 Fingers	Left/Right	Audio Track Prev/Next

System Requirements
Software:
Linux (Ubuntu / Jetson / Debian)
Python 3.x
OpenCV
MediaPipe
playerctl
xdotool
pactl

Install Dependencies:
pip install opencv-python mediapipe
sudo apt install playerctl xdotool pulseaudio-utils
How to Run:
python3 gesture_control.py
Press q to exit.

Features:
Real-time hand tracking
Analog smooth volume control
Swipe-based navigation
Cooldown system to avoid repeated triggers
Single-hand optimized

Future Improvements:
Multi-hand support
Gesture customization
AI gesture classification model
GUI overlay improvements

👨‍💻 Author
Adhithyan
