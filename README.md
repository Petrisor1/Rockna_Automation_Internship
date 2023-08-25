# Setup Appium needed dependencies

## JDK

1. Go to https://www.oracle.com/java/technologies/downloads/#jdk17-windows, download and install JDK.
2. Find and copy the JAVA bin path (should be similar to C:\Program Files\Java\jdk17.0.8\bin)
3. Add the copied path as a new Environment Variable using steps: https://docs.oracle.com/en/database/oracle/machine-learning/oml4r/1.5.1/oread/creating-and-modifying-environment-variables-on-windows.html.
4. Verify if previous steps worked by opening a terminal and typing _java -version_. If it returns the java version, you're good.

## Android JDK

1. Go to https://developer.android.com/studio, scroll down, download the Windows zip folder and extract it.
2. Open the extracted folder and click on SDK Manager app. (this should trigger an installation)
3. In the installer, in the Tools section, select the Android SDK Tools, Platform-tools and Build-tools (only the latest version, not all of them) and select the latest 6 Android versions.
4. Find and copy the extracted Android folder path and add it as a new Environment Variable called Android_Home.
5. Verify if previous steps worked by opening a terminal and typing _android_. If the SDK Manager opens, it worked.
6. Open the extracted folder and click on AVD Manager app to create and start emulators.

## Node JS

1 . Go to https://nodejs.org/ro, download and install the recommended version of NodeJS. 2. Run node -v and npm -v in the terminal to verify if it worked

## Appium

1. Open a terminal and run _npm i -g appium_.
2. Run _appium_ to open server.

## Appium Inspector (needed for gathering selectors)

1. Go to https://github.com/appium/appium-inspector/releases and download the Appium-Inspector-windows-//latest-version//.exe
2. Install and run the application
3. Go to Desired Capabilities tab and add the capabilities from wdio.conf.js (add the full path for the app) and click Start Session.

# Setup the testing application

1. Add the apk file to a tmp folder here in the project.
2. Go to wdio.conf.js and change the path for the app to test in the 'appium:app' capability.
3. Run tests executing _npm run wdio_ in a terminal.
