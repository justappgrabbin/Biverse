# Biverse

Source snapshot: `biverse-guide-synthia-mesh-complete-20260725.zip` (22,413,948 bytes).

SHA-256: `a0a2de265f41293dc54520116fd67be089acb836b3379ddad81ab7f17a6da752`

Upload the unchanged ZIP to the repository root. This repository is public; review the archive before publishing it.

## Android

The Android build is a client for the original React frontend and its Python FastAPI calculation service. It does not bundle a Python interpreter or Swiss Ephemeris into the APK. The client uses the included built frontend and forwards API calls to the service address configured inside the app.

To run the backend from the extracted archive on a supported Python host:

```sh
cd biverse-guide
python -m pip install -r requirements-web.txt
python -m uvicorn human_design.web_api:app --host 127.0.0.1 --port 8000
```

For a remote host, configure an HTTPS reverse proxy and use its HTTPS URL in the app. The local default is `http://127.0.0.1:8000` (a backend on the Android device itself).

The original source and data are preserved in the ZIP. The Android workflow, when installed, builds a debug APK from the included frontend and publishes it as a GitHub Actions artifact.
