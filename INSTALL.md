# Install WatchReserve

Download `WatchReserve-0.2.2.apk` and its `.apk.sha256` file from the [technical preview](https://github.com/brenopoubel0324/watchreserve-app/releases/tag/v0.2.2). Compare the APK's SHA-256 with the value in the checksum file. In PowerShell, use `Get-FileHash -Algorithm SHA256 .\WatchReserve-0.2.2.apk`. On Linux, use `sha256sum -c WatchReserve-0.2.2.apk.sha256`. On macOS, use `shasum -a 256 -c WatchReserve-0.2.2.apk.sha256`.

## From a computer

1. Install [Android SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools). Connect the watch and the computer to the same Wi-Fi network.
2. Enable ADB and wireless debugging in the watch's developer options. Follow the [Wear OS Wi-Fi guide](https://developer.android.com/training/wearables/get-started/debug-wifi) to pair and connect. The pairing port can differ from the connection port.
3. Run `adb devices` and identify the watch. Replace `WATCH_SERIAL` with that identifier and run `adb -s WATCH_SERIAL install -r WatchReserve-0.2.2.apk`. Run the command from the folder with the downloaded APK.

## From an Android phone

On the same Wi-Fi network, use an ADB client such as [Bugjaeger](https://sisik.eu/blog/android/bugjaeger/connect-watch) to pair and connect to the watch. Choose the watch in the client's device selector and [install the downloaded APK](https://sisik.eu/blog/android/bugjaeger/sideload-apk-files) from its package screen.

## After installation

Turn off debugging and follow the [shortcut setup](README.md#install-and-set-up). All four published previews use the same package and signing certificate. If Android reports a signing mismatch, keep your current installation until you decide how to preserve its settings. A local debug build may use another signing key.
