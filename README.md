# Assignment 1: Stone Dodger Game

An interactive Android arcade game where the player controls a car across three lanes and avoids falling obstacles.

---

## 📝 Description

**Stone Dodger Game** is a lane-based survival game developed for Android.
The player starts with **3 lives** and must navigate between the **left**, **middle**, and **right** lanes to avoid stones falling from the top of the screen.

The game includes real-time UI updates, collision detection, life tracking, vibration feedback, and a custom game-over dialog.

---

## 🚀 Features

* **Dynamic Gameplay**
  Stones fall continuously from the top of the screen, requiring quick reflexes and lane switching.

* **Lane Navigation**
  The player can move the car between three lanes using Left and Right controls.

* **Life System**
  The player starts with 3 lives, represented by heart icons.
  Each collision removes one life.

* **Collision Detection**
  The game detects when a falling stone reaches the same lane as the player's car.

* **Haptic & Visual Feedback**

  * Device vibration on collision
  * Toast message displaying `"Crash"` when the player hits a stone

* **Game Over Sequence**
  When all lives are lost, the game loop stops and a custom game-over dialog is displayed.

---

## 🛠️ Tech Stack

| Category              | Technology                   |
| --------------------- | ---------------------------- |
| **Language**          | Java                         |
| **Platform**          | Android                      |
| **Minimum SDK**       | 24+                          |
| **Main Activity**     | AppCompatActivity            |
| **UI Components**     | Google Material Components   |
| **Controls**          | ExtendedFloatingActionButton |
| **Layout Management** | LinearLayout                 |
| **Game Loop**         | Handler / Runnable           |

---

## 🧱 Architecture

The project is organized using a simple separation between UI, game logic, and device feedback.

| Component            | Responsibility                                                       |
| -------------------- | -------------------------------------------------------------------- |
| `MainActivity`       | Handles UI updates, button controls, game loop, and screen rendering |
| `GameManager`        | Manages the 9x3 game matrix, stone movement, collisions, and lives   |
| `SignalManager`      | Singleton helper class for Toast messages and vibration feedback     |
| `Handler / Runnable` | Controls timed stone movement and continuous gameplay updates        |

---

## 🕹️ How to Play

1. **Launch the App**
   The game starts automatically when the app opens.

2. **Move the Car**

   * Press the **Left** button to move one lane left.
   * Press the **Right** button to move one lane right.

3. **Avoid Stones**
   Stones fall from the top of the screen.
   Move between lanes to avoid them.

4. **Lose Lives**
   If a stone reaches the bottom row while the car is in the same lane, the player loses one life.

5. **Game Over**
   When all 3 hearts disappear, the game ends and a custom dialog is displayed.

---

## 📂 Project Structure

```text
com.example.assignment1/
├── MainActivity.java      # UI Controller and Game Loop
├── GameManager.java       # Game logic, matrix handling, stone movement, and collisions
├── SignalManager.java     # Toast and vibration helper using Singleton pattern
└── ...
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/EmilyMyaskovski/assignment1.git
```

### 2. Open in Android Studio

Open the cloned project folder using **Android Studio**.

### 3. Check Dependencies

Make sure the following dependencies exist in your `build.gradle` file:

```gradle
implementation 'androidx.appcompat:appcompat:1.6.1'
implementation 'com.google.android.material:material:1.10.0'
implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
```

### 4. Build and Run

Build the project and run it on either:

* Android Emulator
* Physical Android device

---

## 📱 Requirements

* Android Studio
* Android device or emulator
* Minimum SDK 24+
* Java support enabled in the project

---

## 📄 License

This project was created as part of an Android development course assignment.

---

## 👩‍💻 Author

**Emily Myaskovski**
GitHub Profile: `https://github.com/Emily`
