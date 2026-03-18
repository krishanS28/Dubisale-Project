# System Requirements

Globally installed node
Globally installed react-native CLI
Install CodePush globally and get keys for your app.

# Installation

Clone the project from git using the https url

> \$ git clone [project_url]

# Available Scripts

## npm install

Install node_modules for the project

> \$ npm i

If getiing error of dependency use:

> \$ npm i --f

## npm start

Runs your app in development mode.
Sometimes you may need to reset or clear the React Native packager's cache. To do so, you can pass the --reset-cache flag to the start script:

> \$ npx react-native start

## npm run ios

Like npm start, but also attempts to open your app in the iOS Simulator if you're on a Mac and have it installed.
(<https://reactnative.dev/docs/environment-setup>)

### Simulate for iOS

Method One

Open the project in XCode from ios/NativeStarterKit.xcodeproj
Hit the play button.

Method Two

Run the following command in your terminal

> \$ npx react-native run-ios

## npm run android

Like npm start, but also attempts to open your app on a connected Android device or emulator.

### Simulate for Android

Make sure you have an Android emulator installed and running.
Run the following command in your terminal

> \$ npx react-native run-android

# Release

## Steps to create Release APK (For local device installation)

1. Navigate to project root folder, and open terminal there.
2. In terminal navigate to android folder command : **cd android/**
3. Here run command: **./gradlew assembleRelease**
4. Once command is finished and you get the message: **Build Successful**, navigate to project root directory using file explorer, from here navigate to **android->app->build->outputs->apk->release**.
5. Here we find the apk file which can then be installed on a device using diawi (Open diawi in chrome)

## Steps to create Release AAB (For upload to play store)

> Note: Before following these steps, update your **android/app/build.gradle** file for variables **versionCode** and **versionName** based on previous uploaded versions to playstore

1. Navigate to project root folder, and open terminal there.
2. In terminal navigate to android folder command : **cd android/**
3. Here run command: **./gradlew bundleRelease**
4. Once command is finished and you get the message: **Build Successful**, navigate to project root directory using file explorer, from here navigate to **android->app->build->outputs->bundle->release**.
5. Here we find the aab file which can then be uploaded to play store console.

## For iOS

1. Start Xcode
2. Open the project or workspace
3. Update the version and build numbers
4. In the top menu, select Generic iOS Device as the build destination if no actual device is connected
5. Menu, Project, Archive
6. Click Distribute
7. Sign in as your apple developer account
8. Submit to app store
9. Wait for the confirmation

# Usage

Once setup is done you need to follow the final setup with the installer.
make sure you give READ/WRITE permission to your folder.

