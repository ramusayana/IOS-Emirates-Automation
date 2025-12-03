iOS UI tests – XCUITest (XCUI) (outline)

> This section explains how iOS UI tests would be run, assuming there is an Xcode project with a UITest target.

### 5.1 Typical project layout

- Xcode project: `ios-app/YourApp.xcodeproj`  
- UI test target: `YourAppUITests`  
- Test file example: `YourAppUITests/LoginUITests.swift`

### 5.2 Run XCUITests from Xcode

1. Open the Xcode project (for example `ios-app/YourApp.xcodeproj`) in **Xcode**.  
2. In the scheme selector, choose the **UITests** scheme (e.g. `YourAppUITests`).  
3. Choose an iOS Simulator (for example, iPhone 15).  
4. Press **⌘ + U** (Command + U) or go to **Product → Test**.

Xcode will:

- Build the main app and the UITest target.  
- Launch the simulator.  
- Run all XCUITest UI tests.

### 5.3 Run XCUITests from the command line

From the `ios-app` directory:

```bash
xcodebuild \
  -scheme YourAppUITests \
  -destination 'platform=iOS Simulator,name=iPhone 15,OS=latest' \
  test
```

This does the same as running tests from within Xcode, but via the terminal (useful for CI/CD pipelines).

***

## 6. Summary

- Use **`mvn test`** to run Java API/component tests for the Loyalty Points service.  
- Use **`java -cp ... LoyaltyPointsService`** to start the API locally on port 8080.  
- Use **Android Studio / `./gradlew connectedAndroidTest`** to run Espresso tests on Android.  
- Use **Xcode / `xcodebuild ... test`** to run XCUITest UI tests on iOS.
