# Safety Recorder Pro 🛡️

**Safety Recorder Pro** is a high-priority personal safety application designed to record and preserve visual evidence automatically in emergency situations. It features voice-activated recording, background operation on the lock screen, and automatic cloud synchronization.

## Key Features

-   **Voice-Activated Recording:** Trigger recording instantly by saying keywords like "Help", "Emergency", or "Tabang" (Tagalog).
-   **Lock Screen Support:** Continues monitoring and recording even when the device screen is locked or in deep sleep.
-   **Visual Evidence Stamping:** Automatically stamps videos with a real-time **Timestamp** and the **Safety Recorder Pro** watermark.
-   **Automatic Cloud Sync:** Securely uploads every recording to Firebase Cloud Storage immediately after finalization.
-   **Video Vault:** A local gallery to manage and review recorded evidence.
-   **Privacy-Focused:** No GPS location tracking. Records only when triggered.

## How It Works

1.  **Monitor:** The app runs a low-power background service that listens for specific trigger words.
2.  **Record:** Once a keyword is detected, the app stops the voice listener to free the microphone and immediately starts the camera in the background.
3.  **Sync:** Once the recording is stopped, the file is saved to the internal "SafetyVideos" folder and automatically synced to your private Firebase account.

## Setup Instructions

### Prerequisites
-   Android 10 (API 29) or higher.
-   Firebase Project with Authentication and Storage enabled.
-   Google Cloud Console configuration for OAuth (for Google Sign-In).

### Installation
1.  Clone the repository.
2.  Add your `google-services.json` to the `app/` directory.
3.  Build and run using Android Studio.
4.  Grant permissions for **Camera**, **Microphone**, and **Foreground Services**.

## Permissions Used
-   `CAMERA`: For recording video evidence.
-   `RECORD_AUDIO`: For voice trigger monitoring and video audio.
-   `FOREGROUND_SERVICE`: To remain active in the background.
-   `WAKE_LOCK`: To prevent the CPU from sleeping during an emergency.
-   `RECEIVE_BOOT_COMPLETED`: To restart the safety monitor automatically after a phone reboot.

## License
Licensed under the **Apache License, Version 2.0**. See the `LICENSE` file for more details.

---
*Created for personal safety and accountability.*
