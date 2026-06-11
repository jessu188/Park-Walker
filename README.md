# 🌿 Park Walker

A simple, clean Android app for people who walk laps in a park and want to track their progress without any fuss. No account needed, no internet required — everything stays on your device.

---

## Features

**🏃 Round Tracker**
Tap once per lap to count your rounds. The app automatically calculates your total steps and tracks elapsed time with a live stopwatch.

**📊 Customizable Settings**
Set your steps per round (default: 400) and optionally define a target — by rounds or total steps. A progress bar appears when a target is active.

**📋 Session History**
Every completed session is saved locally with the date, rounds, steps, and duration. Clear history anytime.

**⏱ Independent Stopwatch**
A separate lap stopwatch for free-form timing. Records individual lap times, highlights your fastest and slowest laps, and runs completely independent of the tracker.

---

## Tech Stack

- **Android** (Java)
- **WebView** wrapping a single-file HTML/CSS/JS app
- **localStorage** for persistent settings and history
- No external libraries, no backend, no tracking

---

## Getting Started

### Prerequisites
- Android Studio (latest stable)
- Android device or emulator running Android 5.0+ (API 21+)

### Build & Install

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/ParkWalker.git
   ```

2. Open the `ParkWalker` folder in **Android Studio**

3. Let Gradle sync (happens automatically on first open)

4. Build the APK:
   **Build → Build Bundle(s) / APK(s) → Build APK(s)**

5. Find the APK at:
   ```
   app/build/outputs/apk/debug/app-debug.apk
   ```

6. Transfer to your Android device and install
   *(Enable "Install from unknown sources" in your phone settings if prompted)*

### Or run directly on a connected device

1. Enable **Developer Options** on your phone (tap *Build Number* 7 times in Settings → About Phone)
2. Enable **USB Debugging**
3. Connect your phone via USB
4. Press the ▶ **Run** button in Android Studio

---

## Project Structure

```
ParkWalker/
├── app/
│   ├── src/main/
│   │   ├── assets/
│   │   │   └── index.html        # Full app UI (HTML/CSS/JS)
│   │   ├── java/com/parkwalker/
│   │   │   └── MainActivity.java # WebView host
│   │   ├── res/
│   │   │   ├── layout/activity_main.xml
│   │   │   ├── values/styles.xml
│   │   │   └── mipmap-*/         # Launcher icons
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── gradle/
├── build.gradle
└── settings.gradle
```

---

## How to Use

1. Open the app — you land on the **Tracker** tab
2. Tap **▶ Start** to begin a new session
3. Tap the large **Complete 1 Round** button after each lap
4. Watch your rounds, steps, and time update live
5. Tap **⏹ End Activity** when done — the session is saved to History
6. Switch to **History** to review past sessions
7. Switch to **Stopwatch** for a free lap timer

---

## License

This project is open source and available under the [MIT License](LICENSE).

---

*Built for daily walkers who just want a tap-and-go tracker.*
