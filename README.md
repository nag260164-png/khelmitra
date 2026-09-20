# KhelMitra - Android Mobile Gaming Application

KhelMitra is a comprehensive, mobile-first sports & casual gaming platform featuring 4 skill games (Call Break, Teen Patti, Ludo, Rummy), real-time Live Cricket scores, and a 100% free-to-play virtual coin economy.

---

## 📱 Android APK Build Instructions

The complete native Android project is configured using Capacitor and Gradle.

### Option 1: Build with Android Studio (Recommended GUI)

1. Extract `khelmitra-android-project.zip` (or the `android/` directory).
2. Open **Android Studio**.
3. Select **Open an Existing Project** and browse to the extracted `android` folder.
4. Allow Gradle to perform the initial sync (downloads required Android SDK & Gradle wrappers).
5. From the top menu, go to:
   **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. Once the build finishes, click **locate** in the popup notification, or find the APK here:
   `android/app/build/outputs/apk/debug/app-debug.apk`
7. Transfer `app-debug.apk` to any Android phone or test via an Android emulator.

---

### Option 2: Build with Terminal / Command Line (CLI)

Ensure you have Java JDK 17+ and the Android SDK installed:

```bash
# 1. Navigate to the Android directory
cd android

# 2. Build the Debug APK
./gradlew assembleDebug

# For Windows PowerShell / CMD:
# .\gradlew.bat assembleDebug

# 3. Locate the output APK:
# android/app/build/outputs/apk/debug/app-debug.apk
```

To run directly on a connected USB device with USB debugging enabled:

```bash
npx cap run android
```

---

### Option 3: Instant Android PWA Installation

You can also install KhelMitra directly to your Android home screen:
1. Open the app in **Google Chrome** on your Android device.
2. Tap the **APK** badge in the header or tap the browser menu (**⋮**).
3. Tap **"Add to Home screen"** or **"Install app"**.
4. The app installs as a standalone Android application with offline caching and native app drawer icon!

---

## 🎮 Included Skill Games & Features

1. **Call Break Master**: 4-player trick-taking game with 5 rounds, bidding phase, Spades trump rule, and score tracking.
2. **Teen Patti Royal**: 3-card Indian table game with Blind, Chaal, Pack, Show, and card ranking algorithms.
3. **Khel Ludo Classic**: 2-4 player board game with 3D animated rolling dice, 8 safe star spots ⭐, token capturing, and home paths.
4. **Indian Rummy**: 13-card game with Pure Sequence validation, Sets, Discard & Draw piles, and Declare validation.
5. **Live Cricket Score API**: Automatic 10-second polling scorecard, ball-by-ball commentary, runs, wickets, CRR, and RRR.
6. **Virtual Economy**: 100% Free Virtual Coins, Daily Login Streaks, Lucky Wheel Rewards, and zero real-money gambling.

---

## ⚙️ Android Configuration Details

- **Package Name**: `com.khelmitra.gaming`
- **Application Label**: `KhelMitra`
- **Min SDK**: API 26 (Android 8.0 Oreo)
- **Target SDK**: API 35 (Android 15)
- **Permissions**: `INTERNET`, `ACCESS_NETWORK_STATE`, `VIBRATE`
- **Native Bridge**: Capacitor 8.5+ with Android WebKit
