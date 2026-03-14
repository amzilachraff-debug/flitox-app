# 🚀 FLITOX — Build Guide

## Method 1: Android Studio (Easiest — 5 minutes)

### Step 1 — Install Android Studio
Download from: https://developer.android.com/studio (free)

### Step 2 — Open the project
1. Open Android Studio
2. Click **"Open"**
3. Select the `flitox-app` folder
4. Wait for Gradle sync (~2 min first time)

### Step 3 — Build APK
```
Build → Build Bundle(s)/APK(s) → Build APK(s)
```
APK will be at:
```
flitox-app/app/build/outputs/apk/debug/app-debug.apk
```

### Step 4 — Install on phone
- Connect phone via USB (enable Developer Options + USB Debugging)
- Click **Run** ▶ in Android Studio

---

## Method 2: Command Line (if you have Android SDK)

```bash
# Set your Android SDK path
export ANDROID_HOME=/path/to/your/sdk

# Build debug APK
./gradlew assembleDebug

# APK location:
# app/build/outputs/apk/debug/app-debug.apk
```

---

## Method 3: Online (No installation needed)

1. Create a free account at **appetize.io** or **browserstack.com**
2. Upload the APK after building

---

## Project Structure
```
flitox-app/
├── app/
│   ├── src/main/
│   │   ├── AndroidManifest.xml
│   │   ├── assets/
│   │   │   └── index.html          ← Your FLITOX app
│   │   ├── java/com/achraf/flitox/
│   │   │   └── MainActivity.java   ← WebView wrapper
│   │   └── res/
│   │       ├── mipmap-*/           ← App icons
│   │       └── values/             ← Theme & strings
│   └── build.gradle
├── build.gradle
├── settings.gradle
└── gradle.properties
```

## App Details
- **Package:** com.achraf.flitox
- **Min Android:** 5.0 (API 21) — covers 99% of devices
- **Target Android:** 14 (API 34)
- **Version:** 1.0
