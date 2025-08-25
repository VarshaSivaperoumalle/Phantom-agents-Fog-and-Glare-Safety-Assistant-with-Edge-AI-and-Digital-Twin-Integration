# Phantom-agents-Fog-and-Glare-Safety-Assistant-with-Edge-AI-and-Digital-Twin-Integration
TITLE - Smart Fog and Glare Safety Assistant with Edge AI and Digital Twin

Overview
This project is a real-time road safety solution designed to improve driving visibility and reduce accident risks caused by fog, glare, and driver fatigue. Using edge AI, it processes multi-spectral camera inputs to detect obstacles, monitor driver alertness, and provide instant warnings. A digital twin component logs critical events for later analysis, enabling continuous improvement and integration with fleet safety systems.

Tech Stack

Hardware:
Dual Camera (Visible + Thermal)
Edge AI Processing Unit (NVIDIA Jetson Nano / Raspberry Pi 5 with Coral TPU)
HUD Display for driver alerts

Software / AI Models:
YOLOv5-tiny for object detection
BlazeFace for driver fatigue monitoring
OpenCV for image processing and camera fusion
TensorFlow Lite / TensorRT for optimized inference
SQLite for offline digital twin event storage
PyQt5 for GUI and HUD interface

Setup
Mount the dual camera system on the vehicle dashboard or windshield.
Connect the cameras to the edge AI device (Jetson Nano / Raspberry Pi with Coral TPU).
Install required Python libraries and dependencies (requirements.txt).
Launch the application to start real-time hazard detection and logging.
View alerts directly on the HUD display while driving.

Features
Enhanced Visibility: Fusion of thermal and visible imaging to mitigate fog and glare.
Driver Fatigue Monitoring: Detects blink rate, gaze direction, and head movements.
Real-Time Alerts: Provides immediate warnings via HUD display and audio signals.
Offline Operation: Works without internet connectivity, ideal for remote areas.
Digital Twin Event Logging: Stores critical events for analysis and reporting.
Cost-Effective: Retrofittable solution suitable for existing vehicles.

Technical Workflow

Input Acquisition: Captures frames from visible and thermal cameras.
Pre-Processing: Aligns and fuses multi-spectral data using OpenCV.
AI Inference:
YOLOv5-tiny detects obstacles and road hazards.
BlazeFace monitors driver fatigue indicators.
Decision Layer: Triggers alerts if a hazard or fatigue condition is detected.
Data Logging: Saves key events to SQLite for post-drive analysis (digital twin).
