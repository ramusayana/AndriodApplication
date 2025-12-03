Android UI tests – Espresso (outline)

> This section explains how Android UI tests would be run, assuming there is an Android app module with Espresso tests.

###1 Typical project layout

- Android app module, for example:  
  `android-app/app/`
- Espresso test classes under:  
  `android-app/app/src/androidTest/java/...`

An example test file might be: `LoginEspressoTest.kt`.

###2 Run Espresso tests from Android Studio

1. Open the Android module (e.g. `android-app/`) in **Android Studio**.  
2. Connect a device or start an Android Emulator.  
3. In the Project view, right‑click the test class (for example `LoginEspressoTest`) and choose **Run**.  

Android Studio will:

- Build the app.  
- Install it on the device/emulator.  
- Run all Espresso tests in the `androidTest` package.

### 3 Run Espresso tests from the command line

From the Android module root (where `gradlew` is located):

```bash
./gradlew connectedAndroidTest
```

This will:

- Build the app in debug mode.  
- Deploy it to the connected device/emulator.  
- Run all instrumented tests (Espresso).

***
