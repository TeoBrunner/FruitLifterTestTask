
https://github.com/user-attachments/assets/28179d85-a393-4870-b4d2-7c0f19ff0981

# Fruit Lifter 🍎

**A mobile-first, physics-based interaction demo built in Unity for a technical test.**
Completed in 8 hours with a focus on smooth mobile controls, clean architecture, and satisfying physical interactions.

![Play](https://img.shields.io/badge/Play-Itch.io-orange)

## 🎮 Overview
**Fruit Lifter is a first-person mobile interaction prototype where you can walk around, pick up objects, examine them, and throw them with realistic physics.**

The project demonstrates:
- Mobile-optimized dual-control scheme (movement + look)
- Physics-based pickup & throw mechanics
- Clean dependency injection with Zenject
- Event-driven input handling
 
## 📱 Controls

**The game is designed for mobile touch screens:**
- Left Joystick → Move forward/backward, strafe left/right
- Drag anywhere else on screen → Look around (rotate camera)
- Tap on a pickupable object → Pick it up (object becomes invisible to physics, appears in hand)
- Throw Button (appears when holding an object) → Throw the object forward with physical impulse

*Note: No PC controls are implemented—this is a mobile-first experience.*
🛠️ Tech Stack

![Unity](https://img.shields.io/badge/Unity-2022.3+-black?style=flat&logo=unity)
![Zenject](https://img.shields.io/badge/DI-Zenject-blue)
![Platform](https://img.shields.io/badge/Platform-WebGL%20%7C%20Mobile-green)

- Unity 6.3+ – Game engine
- Zenject – Dependency injection framework
- Unity UI & EventSystem – Touch input handling

## 🧱 Architecture & Key Scripts

**The project follows a modular, DI-driven design**
*Core Scripts*
`Item`: Represents a pickupable object. Can be made kinematic/enabled for physics.

`ItemPicker`:	Handles picking and throwing logic. Listens to touch input via SwipeZone.

`MovementController`:	Moves the player based on Joystick input in FixedUpdate.

`CameraController`:	Rotates the camera based on swipe input from SwipeZone.

`SwipeZone`:	UI component that emits touch and drag events.

`PlayerInstaller / UIInputInstaller`:	Zenject installers that bind scene-specific dependencies.

**Dependency Injection**
- Zenject is used to inject Joystick, SwipeZone, Camera, Button references.
- Separation between input, logic, and presentation layers.
- Easy to replace components (e.g., different input schemes).

## 🚀 Installation & Running
- Clone the repository
- Open in Unity 2022.3+
- Open the main scene (Assets/Project/Scenes/MainScene.unity)
- Ensure Zenject project context is set up (usually auto-generated)
- Press Play – Use Unity Remote or build to mobile for best experience.

## 📦 Build

**A WebGL build is available here:**
👉 https://teobrunner.itch.io/fruit-lifter

You can play directly in your browser (mobile touch supported).
🧠 What This Project Shows
- ✅ Mobile-first touch input system
- ✅ Clean separation of input, logic, and physics
- ✅ Event-driven architecture (no tight coupling)
- ✅ Quick iteration under time constraints (8-hour test)
- ✅ Zenject for scalable dependency management

📌 Notes

- This was a time-boxed technical test (8 hours).
- Focus was on core mechanics and clean code, not polish or content.
- The architecture allows easy extension (e.g., adding new items, input methods, platforms).

📄 License

This project is provided as a portfolio piece.
Code may be reused with attribution.

Built with Unity • Delivered in 8 hours • 2025
