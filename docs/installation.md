# Installing StreamVR3D

These are draft instructions for a future approved release. No official public download is available yet.

## Before you start

- A supported Quest headset, a Windows PC, and a USB-C cable that carries data.
- Developer Mode enabled for the headset using Meta's current developer setup guidance.
- A signed Quest APK and the matching Windows setup package from the same official StreamVR3D release.
- For the current Windows companion design, Android Studio with **Android SDK Platform-Tools** and **Android SDK Build-Tools** installed through its SDK Manager. Android Studio includes a Java runtime. These tools are free but are obtained directly from Google, not bundled in this draft package. See the [official Android Studio installation guide](https://developer.android.com/studio/install) and [Platform-Tools page](https://developer.android.com/tools/releases/platform-tools).

## Prepare the Windows PC for the current companion

1. Install [Android Studio from Google](https://developer.android.com/studio/install) with its default Android SDK location. Open it once to finish its setup and accept Google's terms if you agree to them.
2. In Android Studio, open **Tools → SDK Manager**, then the **SDK Tools** tab. Select **Android SDK Platform-Tools** and **Android SDK Build-Tools**, choose **Apply**, and let the installation finish. [Google's SDK Manager guide](https://developer.android.com/studio/intro/update) shows this screen.
3. Reopen the StreamVR3D Windows companion so it detects the installed tools. You do not need to write code or open a project in Android Studio.

This free setup path still needs a clean-PC acceptance test before public release.

## Install or update

1. Download both files from the official release page after it opens. Verify their SHA-256 hashes against `SHA256SUMS.txt` from that release.
2. Extract the complete Windows setup ZIP if it is supplied as a ZIP. Keep its files together.
3. Unlock the headset, connect it directly to the PC, and accept the USB debugging prompt inside the headset.
4. Run the Windows installer. Choose **Detect headset**, select the release APK, then choose **Install / update**.
5. Open StreamVR3D from the headset's **Unknown Sources** library.

An update must use the same Android signing certificate as the installed app. The installer should reject a different certificate or a downgrade and preserve app data on a valid update. Do not uninstall the existing app merely to force an update; that may erase local settings and history.

Provider credentials are entered by the user in the app or an explicitly supported secure setup flow. Never send them to support staff.
