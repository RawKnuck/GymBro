# 🏋️ GymBro — Your Personal Gym Tracker

<p align="center">
  <strong>Track lifts. Track protein. Get stronger.</strong>
</p>

<p align="center">
  <a href="https://github.com/RawKnuck69/GymBro/releases/tag/v1.0">
    <img src="https://img.shields.io/badge/version-1.0-blue?style=flat-square" alt="Version 1.0">
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

GymBro is a **personal gym tracking app** designed for one purpose: helping you get stronger, consistently. No social feeds, no fluff — just the tools you need to track your lifting sessions and protein intake.

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

🥩 **Protein Tracker**
- Daily protein intake logging with customizable goals
- Reminder system to stay on track
- Meal-by-meal breakdown

☁️ **Cloud Sync**
- Google Sign-In for cross-device sync
- Firebase-backed data storage
- Guest mode for offline use

---

## 📥 Download

Download the latest APK from the [Releases](https://github.com/RawKnuck69/GymBro/releases) page.

| Version | Date | Download |
|---------|------|----------|
| v1.0 | June 2026 | [gymbro-debug.apk](https://github.com/RawKnuck69/GymBro/releases/tag/v1.0) |

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
