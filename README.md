# Biverse

The Android build is now designed as a self-contained ARM64 APK with the original React interface, embedded Python/FastAPI calculation engine, original IsoHuman astronomy-engine calculator, local SQLite learning stores, and TinyLlama 1.1B Q4_K_M running via llama.cpp. The app declares no INTERNET permission and does not require a separately hosted server.

## Build from the revised archive

Upload the exact revised file `biverse-offline-android.zip` to this repository's root.

SHA-256: `8bf61aaa8809c80f0d1ca8519208be0ec39b606d29a46bc29707ae5692efbac2`

The [Android build workflow](.github/workflows/android.yml) runs on upload or manual dispatch, obtains build-only dependencies and embeds the model weights into the APK. Download the `Biverse-Offline-ARM64-debug` artifact from Actions after a successful build.

Host integration tests passed (22 tests). Native Android compilation and actual on-device inference and airplane-mode testing are still pending. The APK uses the original astronomy-engine local calculation path, not the optional desktop PyHD/Swiss Ephemeris engine. The original separate CLI/mesh sources are preserved; not all have Android execution adapters. Read `android/README.md` in the revised archive for details.

This repository is public. Review the archive's contents before uploading.
