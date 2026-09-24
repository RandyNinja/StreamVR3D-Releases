# Installing StreamVR3D

These are draft instructions for a future approved release. No official public download is available yet.

**Device support notice:** Only Meta Quest 3 has been tested with StreamVR3D. Other Quest models have not been verified. StreamVR3D is a sideloaded Quest app, not a Windows video player.

## Before you start — all methods

- Download the signed **Quest APK** and `SHA256SUMS.txt` from the same official StreamVR3D GitHub release when it becomes available. Check that the APK's SHA-256 matches the published value. You need the Windows setup ZIP only if you choose the StreamVR3D companion method below.
- Use a Meta Quest 3 with a Meta developer account and Developer Mode enabled. Follow [Meta's device setup guide](https://developers.meta.com/horizon/documentation/native/android/mobile-device-setup/).
- Connect the headset to your computer with a **USB-C data cable** and approve the **Allow USB debugging** prompt inside the headset. A charge-only cable will not work. Windows may need [Meta's ADB driver](https://developers.meta.com/horizon/documentation/native/android/mobile-device-setup/) if the headset is not detected.
- After installation, open StreamVR3D from **Library → Unknown Sources** on the headset.

## Option 1: Meta Quest Developer Hub

If you already use Meta Quest Developer Hub (MQDH), you can install the official APK without the StreamVR3D Windows companion or Android Studio.

1. Open MQDH and connect your developer-mode Quest 3 by USB. Approve the headset's USB debugging prompt.
2. In **Device Manager → Apps**, drag the StreamVR3D Quest APK into the window or choose **Add Build** and select the APK.
3. Wait for installation to finish, then open StreamVR3D from **Library → Unknown Sources**.

Meta's [MQDH deployment guide](https://developers.meta.com/horizon/documentation/spatial-sdk/ts-mqdh-deploy-build/) shows the current controls.

## Option 2: SideQuest Advanced Installer or another APK-capable app

If you already use **SideQuest Advanced Installer**, connect the Quest 3, approve USB debugging, then use its **Install APK file from folder on computer** control to select the official StreamVR3D Quest APK. Wait for the install to finish and open StreamVR3D from **Library → Unknown Sources**. SideQuest's Easy Installer may not offer local APK installation; use the [Advanced Installer from SideQuest's official download page](https://sdq.st/download). [SideQuest's support answer](https://sidequestvr.com/support/148500/apk-installation-on-sidequest-124-version) explains the distinction. Button names may change with SideQuest updates.

Another sideloading application can be used if it supports installing a local APK on a developer-mode Quest. Select the official StreamVR3D APK and follow that application's own device-connection and install steps. The StreamVR3D Windows companion and Android Studio are not required for these methods.

## Option 3: Android Platform-Tools (advanced)

If you already use ADB, connect the headset and run the following in a terminal where `adb` is available. [Google provides Platform-Tools directly](https://developer.android.com/tools/releases/platform-tools); Android Studio is not required for this option.

```text
adb devices
adb install -r "path-to-StreamVR3D-Quest.apk"
```

The device should show as `device` before installing. The `-r` option installs over an existing copy while keeping its data. See [Meta's ADB instructions](https://developers.meta.com/horizon/documentation/unity/unity-env-device-setup/) and [Google's ADB reference](https://developer.android.com/tools/adb). Meta says apps installed this way do not receive Quest Cloud Backup, so do not rely on cloud backup for local settings or history.

## Option 4: StreamVR3D Windows companion

The optional Windows companion helps install or update the Quest APK. This route requires a Windows PC and a USB-C data cable. For the current companion design, install Android Studio with **Android SDK Platform-Tools** and **Android SDK Build-Tools** through its SDK Manager. Android Studio includes a Java runtime. These tools are free and obtained directly from Google; they are not bundled in the StreamVR3D package. See [Google's Android Studio guide](https://developer.android.com/studio/install).

1. Install Android Studio from Google with its default Android SDK location. Open it once to finish setup and accept Google's terms if you agree to them.
2. In Android Studio, open **Tools → SDK Manager → SDK Tools**. Select **Android SDK Platform-Tools** and **Android SDK Build-Tools**, choose **Apply**, and let installation finish. [Google's SDK Manager guide](https://developer.android.com/studio/intro/update) shows this screen.
3. Download the matching StreamVR3D Windows setup ZIP from the same official release and extract it completely. Keep its files together.
4. Reopen the StreamVR3D Windows companion so it detects the installed tools. Connect and unlock the headset, then approve USB debugging inside it.
5. In the companion, choose **Detect headset**, select the release APK, then choose **Install / update**.
6. Open StreamVR3D from the headset's **Unknown Sources** library.

This companion route still needs a clean-PC acceptance test before public release.

## Updating without losing local data

Install the newer official APK **over the existing app**. Do not uninstall StreamVR3D or clear its data just to force an update: [uninstalling erases app data](https://developer.android.com/google/play/app-updates), including local settings and watch history. An in-place update needs the same app ID and signing certificate and a suitable version code. If an installer reports a signature mismatch or downgrade, stop and check the official release and [support guide](../SUPPORT.md) before taking further action.

Provider credentials are entered by the user in the app or an explicitly supported secure setup flow. Never send them to support staff.
