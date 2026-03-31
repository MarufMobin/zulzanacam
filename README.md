# 📷 ZulzanaCam

A Flutter-based camera and media application that supports photo capture, video recording, audio playback, and media management.

---

## 🚀 Features

- 📸 Camera capture (photo & video)
- 🖼️ Image picking from gallery
- 🎵 Audio playback with `assets_audio_player`
- 🎬 Video playback with `video_player`
- 🎚️ Syncfusion sliders for media controls
- 📁 File & path management
- 🔔 Toast notifications
- 💾 Media caching with `flutter_cache_manager`
- 🔐 Runtime permission handling

---

## 🛠️ Tech Stack

| Package | Purpose |
|---|---|
| `camera` | Camera preview & capture |
| `image_picker` | Pick images/videos from gallery |
| `video_player` | Video playback |
| `assets_audio_player` | Audio playback |
| `syncfusion_flutter_sliders` | Media seek/progress sliders |
| `permission_handler` | Runtime permissions |
| `flutter_cache_manager` | Caching media files |
| `path_provider` | Access device directories |
| `path` | File path utilities |
| `image` | Image processing |
| `get` | State management & navigation |
| `fluttertoast` | Toast messages |

---

## 📋 Requirements

- Flutter SDK `^3.8.1`
- Dart SDK `^3.8.1`
- Android `minSdk 21+`
- Android `compileSdk 36`
- NDK `27.0.12077973`
- Java 17

---

## ⚙️ Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/zulzanacam.git
cd zulzanacam
```

### 2. Install dependencies

```bash
flutter pub get
```

### 3. Run the app

```bash
flutter run
```

### 4. Build release APK

```bash
flutter build apk --release
```

---

## 🔐 Permissions

The following permissions are required and declared in `AndroidManifest.xml`:

| Permission | Reason |
|---|---|
| `CAMERA` | Capture photos and videos |
| `RECORD_AUDIO` | Record audio/video |
| `READ_MEDIA_IMAGES` | Access images (Android 13+) |
| `READ_MEDIA_VIDEO` | Access videos (Android 13+) |
| `READ_EXTERNAL_STORAGE` | Access media (Android 12 and below) |
| `WRITE_EXTERNAL_STORAGE` | Save media (Android 12 and below) |
| `INTERNET` | Network requests |
| `ACCESS_NETWORK_STATE` | Check connectivity |

---

## 📁 Project Structure

```
zulzanacam/
├── android/                  # Android native configuration
│   ├── app/
│   │   └── build.gradle.kts  # App-level Gradle config
│   └── build.gradle.kts      # Root Gradle config
├── ios/                      # iOS native configuration
├── lib/                      # Dart source code
│   └── main.dart             # App entry point
├── assets/                   # Static assets
├── pubspec.yaml              # Dependencies & metadata
└── README.md
```

---

## 🐛 Known Issues & Fixes

### JVM Target Mismatch
If you encounter `Inconsistent JVM Target Compatibility`, ensure `android/build.gradle.kts` forces Java 17 across all subprojects.

### Namespace Error (flutter_barcode_scanner)
Add `namespace "com.amolg.flutterbarcodescanner"` to the plugin's `build.gradle` located in your pub cache, or replace with `mobile_scanner`.

### Deprecation Warnings (sqflite_android)
Warnings about deprecated `Locale` and `Thread.getId()` in `sqflite_android` are harmless and originate from the package source — they do not affect functionality.

---

## 📄 License

This project is private and not published to pub.dev.

---

## 👨‍💻 Author

Developed by **Md Maruf**  
Contact: appdevmaruf@gmail.com