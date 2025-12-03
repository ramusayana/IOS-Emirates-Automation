iOS UI tests – XCUITest (XCUI) (outline)

> This section explains how iOS UI tests would be run, assuming there is an Xcode project with a UITest target.

### 1 Typical project layout

- Xcode project: `ios-app/YourApp.xcodeproj`  
- UI test target: `YourAppUITests`  
- Test file example: `YourAppUITests/LoginUITests.swift`

### 2 Run XCUITests from Xcode

1. Open the Xcode project (for example `ios-app/YourApp.xcodeproj`) in **Xcode**.  
2. In the scheme selector, choose the **UITests** scheme (e.g. `YourAppUITests`).  
3. Choose an iOS Simulator (for example, iPhone 15).  
4. Press **⌘ + U** (Command + U) or go to **Product → Test**.

Xcode will:

- Build the main app and the UITest target.  
- Launch the simulator.  
- Run all XCUITest UI tests.

### 3 Run XCUITests from the command line

From the `ios-app` directory:

```bash
xcodebuild \
  -scheme YourAppUITests \
  -destination 'platform=iOS Simulator,name=iPhone 15,OS=latest' \
  test
```



