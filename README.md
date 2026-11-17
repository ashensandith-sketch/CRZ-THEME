# CR-Z Blue Launcher v0.3 — Android Studio source

Designed for a T100 head unit (reported Android 15, 4 GB RAM). **Not compiled or device-tested.**

## New in v0.3
- Updated electric-blue CR-Z background image
- Assign and remember preferred apps for Music, FM Radio, and Bluetooth Phone (first selection)
- Reset GPS trip distance by tapping the trip readout, with confirmation
- GPS speed automatically falls to zero when location data is stale
- Corrected radio app filtering and app chooser labels

## Build
1. Open this folder in Android Studio with Android SDK 35 installed.
2. Allow Gradle sync, then Build > Build Bundle(s) / APK(s) > Build APK(s).
3. Transfer the debug APK to the head unit and install it while parked.
4. Start as a normal app first. Do not select it as the default Home app until tested.

## Limitations
- The current app is a prototype; not verified to compile on this environment (Android SDK/Gradle unavailable).
- Music playback uses Android media key events and may not control proprietary players.
- FM radio and Bluetooth calling open the selected OEM apps; no internal control APIs are implemented.
- Weather is not live; no weather service is configured.
- Drive timer starts when the launcher opens, not when the vehicle starts.
- Screen scaling is based on a 1600x900 virtual canvas, and should be validated on the device.
- Some UI labels are not yet final.

## Safety
Keep factory Home installed and available; do not modify MCU firmware or factory settings. Only interact with launcher while parked.
