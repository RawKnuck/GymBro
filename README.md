# 🏋️ GymBro — Your Personal Gym Tracker

<p align="center">
  <strong>Track lifts. Track protein. Get stronger.</strong>
</p>

<p align="center">
  <a href="https://github.com/RawKnuck/GymBro/releases/tag/v1.3">
    <img src="https://img.shields.io/badge/version-1.3-blue?style=flat-square" alt="Version 1.3">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/platform-Android-green?style=flat-square" alt="Android">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/built%20with-Capacitor-blue?style=flat-square" alt="Capacitor">
  </a>
</p>

---

## 📱 What is GymBro?

GymBro is a minimalist, distraction-free training companion built for analytical lifters who value science over hype. Unlike generic trackers bloated with social feeds and advertisements, GymBro is engineered for one ultimate goal: **systematic progressive overload**. 

It was designed to solve real-world training constraints, focusing on:

*   **Defeating the "No Microplates" Plateau:** Most Indian gyms lack microplates (like 1.25 kg plates), forcing you to make massive 5 kg jumps that stall progress on weight-sensitive barbell lifts like the Overhead Press and Bench Press. GymBro bypasses this by using rep-range auto-regulation. It advises weight increases only when you have systematically built the raw rep capacity to handle the next step.
*   **Protein Anchoring > Calorie Obsession:** Say goodbye to the tedious chore of tracking every single calorie. GymBro centers its nutrition logic on *protein anchoring*—securing your protein intake target around daily food anchors to deliver 80% of your body composition results with 20% of the cognitive overhead.
*   **Journal-Backed Progression Science:** Progression recommendations are mathematically guided by the Epley and Brzycki 1RM formulas, selecting the worst-case (lowest) estimate to guarantee adaptational safety.
*   **Injury Prevention First:** Built-in neural buffers ensure you never lift beyond your current physical thresholds, keeping your joints healthy and your long-term training sustainable.
*   **Laser-Focused & Analytical:** No distractions. Just pure, clean performance charts, trendlines, and data analytics for lifters who treat self-improvement like an engineering problem.

### Key Features

🏋️ **Lift Tracking & Progression**
- Log sets, reps, and weights for any exercise
- Smart progressive overload recommendations based on exercise science
- RPE-based autoregulation for sustainable gains
- Session history with full analytics

📊 **Analytics Dashboard**
- Track bodyweight over time with interactive charts
- Lift-specific analytics with progression trends
- Volume and intensity tracking

🥩 **Protein Anchor Tracker**
- Daily protein anchor tracking
- Don't worry about tracking the calories
- With minimal effort get most of your gains

☁️ **Cloud Sync**
- Google Sign-In for cross-device sync
- Firebase-backed data storage
- Guest mode for offline use

---

## 📥 Download

Download the latest APK from the [Releases](https://github.com/RawKnuck/GymBro/releases) page.

| Version | Date | Download |
|---------|------|----------|
| v1.3 | June 2026 | [gymbro_v1.3.apk](https://github.com/RawKnuck/GymBro/releases/download/v1.3/gymbro_v1.3.apk) |
| v1.2.1 | June 2026 | [gymbro_v1.2.1.apk](https://github.com/RawKnuck/GymBro/releases/download/v1.2.1/gymbro_v1.2.1.apk) |
| v1.2 | June 2026 | [gymbro_v1.2.apk](https://github.com/RawKnuck/GymBro/releases/download/v1.2/gymbro_v1.2.apk) |
| v1.1.1 | June 2026 | [gymbro_v1.1.1.apk](https://github.com/RawKnuck/GymBro/releases/download/v1.1.1/gymbro_v1.1.1.apk) |
| v1.1 | June 2026 | [gymbro_v1.1.apk](https://github.com/RawKnuck/GymBro/releases/download/v1.1/gymbro_v1.1.apk) |
| v1.0 | June 2026 | [gymbro-debug.apk](https://github.com/RawKnuck/GymBro/releases/download/v1.0/gymbro-debug.apk) |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, JavaScript (vanilla) |
| Mobile | [Capacitor](https://capacitorjs.com/) (Android wrapper) |
| Backend | Firebase (Auth, Firestore) |
| Auth | Google Sign-In (native Android) |
| Build | Gradle + OpenJDK 17 |

---

## 🏗️ Building from Source

### Prerequisites
- Node.js 18+
- Android SDK (Platform 34, Build-Tools 34.0.0)
- JDK 17

### Steps

```bash
# Install dependencies
npm install

# Build web assets for Capacitor
powershell -ExecutionPolicy Bypass -File .\build-dist.ps1

# Sync with Android
npx cap sync android

# Build the APK
cd android
./gradlew assembleDebug
```

The APK will be at `android/app/build/outputs/apk/debug/app-debug.apk`.

---

## 📋 Project Structure

```
GymBro/
├── app.js                  # Main application logic
├── index.html              # App UI
├── style.css               # Styling
├── capacitor.config.json   # Capacitor configuration
├── build-dist.ps1          # Asset build script
├── firebase.json           # Firebase hosting config
├── firestore.rules         # Firestore security rules
├── firestore.indexes.json  # Firestore indexes
├── gymbro-debug.apk        # Pre-built debug APK
├── android/                # Android native project
│   ├── app/
│   │   ├── build.gradle
│   │   ├── google-services.json
│   │   └── src/main/
│   │       ├── java/.../MainActivity.java
│   │       ├── res/values/strings.xml
│   │       └── assets/public/  (synced web assets)
│   ├── build.gradle
│   └── variables.gradle
└── package.json
```

---

## 🔒 Privacy

GymBro stores your data in your own Firebase project. No data is shared with third parties. The app only requests the minimum permissions needed (Google account profile + email for sign-in).

---

## 📄 License

This is a personal project. All rights reserved.

---

<p align="center">
  Built with 💪 by <a href="https://github.com/RawKnuck">Raunak Jalan</a>
</p>
