# React Native Environment Setup

## 1. System Requirements

- **Operating System**: Windows 10 or later (64-bit)
- **CPU**: At least an Intel Core i5 or equivalent
- **RAM**: At least 8 GB (16 GB recommended for smooth performance with simulators)
- **Storage**: 10+ GB of free storage for Android SDK and emulators

## 2. Installation Instructions

Follow these steps to install the necessary tools and dependencies:

### Install Node.js
1. Go to the [Node.js website](https://nodejs.org/).
2. Download the LTS version of Node.js and install it.
3. Verify the installation by running `node -v` and `npm -v` in the terminal.

### Install React Native CLI
1. Open a terminal and run the following command:
    ```bash
    npm install -g react-native-cli
    ```

### Install Android Studio
1. Download and install [Android Studio](https://developer.android.com/studio).
2. During installation, ensure you check these boxes:
    - Android SDK
    - Android SDK Platform
    - Android Virtual Device (AVD) for the emulator
3. Open Android Studio, go to **SDK Manager**:
    - Select **SDK Platforms**: Ensure **Android 12.0 (S)** or later is installed.
    - Select **SDK Tools**: Ensure that **Android SDK Build-Tools** and **Android Emulator** are checked.
4. Set up an Android virtual device (AVD) by clicking **AVD Manager** and creating a new virtual device.

### Set Up Environment Variables
1. Set `ANDROID_HOME` in your system environment variables:
    - Go to **System Properties > Environment Variables**.
    - Add a new user variable named `ANDROID_HOME` and set it to the path of your Android SDK, typically:
      ```bash
      C:\Users\<Your-Username>\AppData\Local\Android\Sdk
      ```
2. Add the following paths to the `Path` variable in **System Variables**:
    ```bash
    %ANDROID_HOME%\platform-tools
    %ANDROID_HOME%\emulator
    ```

### Install Java Development Kit (JDK)
1. Download the latest version of [JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Add the JDK's `bin` directory to the **Path** environment variable.

## 3. Project Creation

- Open a terminal and navigate to the directory where you want to create the app.
- Run the following command to create a new React Native project:
    ```bash
    npx react-native init IncredibleTodoListApp
    ```
- Navigate into the project folder:
    ```bash
    cd IncredibleTodoListApp
    ```

## 4. Running the Project

### Start the Android Virtual Device (AVD)
1. Open Android Studio and click on **AVD Manager**.
2. Start the emulator.

### Run the Project
1. Open the terminal and run:
    ```bash
    npx react-native run-android
    ```
2. This will launch the app in the Android emulator.

## 5. Troubleshooting

Common issues during the setup:

- **Error: `SDK location not found`**:
    - Ensure that the `ANDROID_HOME` environment variable is set correctly.
  
- **Error: `Could not find a suitable Android device`**:
    - Make sure the Android emulator is running.
  
- **Build failed due to missing Java version**:
    - Ensure the correct JDK version is installed, and the path is set in the environment variables.
  
- **Error: `Execution failed for task ':app:mergeDebugResources'`**:
    - Run `npm install` to install any missing dependencies.

## 6. Resources

- [React Native Official Docs](https://reactnative.dev/docs/environment-setup)
- [Stack Overflow React Native Questions](https://stackoverflow.com/questions/tagged/react-native)
- [Node.js Official Site](https://nodejs.org/)
