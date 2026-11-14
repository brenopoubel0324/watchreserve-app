# Compatibility and test results

| Device | Status for v0.2.2 |
| --- | --- |
| Galaxy Watch8 LTE, 40 mm (SM-L325F), Android 16/API 36, firmware L325FXXS3AZF4 | The installed signed APK opened Samsung's own Watch only confirmation. The user confirmed Home double press, tile, and watch face complication in normal use. |
| Galaxy Watch4 and later with Wear OS/API 30 or newer | Target devices. Other models, variants and firmware require a separate check. |
| Tizen-based Galaxy Watch models | Outside the APK's compatibility range. |

The physical test reached the native confirmation without pressing **Turn on**. The Home shortcut reduced the steps needed to reach it from the watch face. The app leaves activation to Samsung's confirmation screen. Samsung explains the [impact of Watch only on smart features](https://www.samsung.com/us/support/answer/ANS10002905/).

The 0.2.2 emulator checks used a circular Wear OS 5/API 34 image and included the shortcut launch while the app panel was already open. The screenshots in the README come from that environment. Full physical checks after restart or process interruption remain pending, and battery-life gains have not been measured.

The Home shortcut depends on Samsung's button picker. The complication depends on the watch face and its slots. Available battery settings vary with the hardware and firmware. If a previously tested direct shortcut stops working, run the Samsung screen check again. Until it is validated, use the public battery or general settings screen offered by the app.
