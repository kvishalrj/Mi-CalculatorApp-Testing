# Mi Calculator Test Automation

This project demonstrates test automation for the Mi Calculator app using **Appium** and **Gradle**. It automates a simple addition operation in the Mi Calculator Android application using an emulator or a physical device.

## Prerequisites

Ensure you have the following installed:

1. **Java Development Kit (JDK)** (version 8 or higher)
2. **Gradle** (version 7 or higher)
3. **Appium** (latest version)
4. **Android SDK** with an emulator or a connected Android device
5. **Node.js** (required for Appium)
6. **Appium Inspector** (optional, for inspecting UI elements)

## Project Structure

```plaintext
micalculatortest/
├── src/
│   ├── main/
│   │   └── java/
│   │       └── micalculatortest/
│   │           └── App.java
├── build.gradle
├── settings.gradle
└── README.md
```

## Dependencies

The `build.gradle` file should include the following dependencies:

```gradle
dependencies {
    implementation 'io.appium:java-client:8.5.1'
}
```

## Setup Instructions

1. **Clone the Repository:**

   ```bash
   git clone <repository_url>
   cd micalculatortest
   ```

2. **Install Dependencies:**

   Ensure Gradle resolves the dependencies by running:

   ```bash
   gradle build
   ```

3. **Start the Appium Server:**

   Run the following command to start the Appium server:

   ```bash
   appium
   ```

4. **Set Up an Android Emulator or Device:**

   - Start an Android Emulator or connect a physical device.
   - Ensure the **Mi Calculator app** is installed on the device.
   - Verify the device is detected using `adb devices`.

5. **Run the Test:**

   Execute the Java program using Gradle:

   ```bash
   gradle run
   ```

   Alternatively, compile and run the program directly with:

   ```bash
   javac -cp <path_to_appium_java_client_jar> App.java
   java -cp <path_to_appium_java_client_jar> App
   ```

## How the Code Works

1. **Capabilities Configuration:**
   - Sets up the device and app-specific details using `UiAutomator2Options`.

2. **Appium Server Connection:**
   - Establishes a connection with the Appium server using the server's URL.

3. **Automated Test Steps:**
   - Launches the Mi Calculator app.
   - Automates a basic addition operation (`9 + 7 = 16`).
   - Verifies the result using UI element inspection.

4. **Output:**
   - The result of the calculation is printed in the console.
   - A boolean value confirms whether the result matches the expected value.

## Sample Output

Upon successful execution, the console will display:

```plaintext
Hello World!
successfully open calculator
true
= 16
```

## Notes

- Ensure the `appPackage` and `appActivity` values match your installed version of Mi Calculator. Adjust them if necessary.
- Update the Appium server URL (`http://127.0.0.1:4723/`) if running Appium on a different machine or port.

## Troubleshooting

1. **Device Not Found:**
   - Ensure the device is properly connected and listed with `adb devices`.

2. **Appium Errors:**
   - Confirm the Appium server is running and accessible at the specified URL.

3. **UI Element Not Found:**
   - Use Appium Inspector to validate the element IDs (`com.miui.calculator:id/...`).

## References

- [Appium Documentation](https://appium.io/docs/en/about-appium/intro/)
- [Gradle Documentation](https://gradle.org/docs/)