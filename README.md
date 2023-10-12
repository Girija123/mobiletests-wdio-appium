# mobiletests-wdio-appium

## About
Currently, this framework has been developed to run scripts in ANDROID platform with an emulator.
The calculator app APK used in this project is in app/android directory

## Tech Stack
- Appium 
- WebdriverIO
- JavaScript

# Getting Started
## Pre-requisites
1. NodeJS 
2. JAVA(jdk) 
3. Andriod(sdk)
4. Set JAVA_HOME & ANDROID_HOME paths in Environment variable

# Installation
## Setup Scripts
Clone the repository into a folder
Go inside the folder and run the following command from terminal/command prompt
```npm install``` 
All the dependencies from package.json would be installed in node_modules folder.

# Run Tests
Create and open an Android emulator to match with the current capabilities set in wdio.config.js. 
```
capabilities: [
    {
      platformName: "Android",
      "appium:deviceName": "Pixel 7",
      "appium:platformVersion": "13.0",
      "appium:automationName": "UiAutomator2",
      "appium:app": path.join(
        process.cwd(),
        "./app/android/Calculator_8.4.1.apk"
      ),
    },
  ],
```
To run the tests:

```npx wdio``` or ```npm run wdio```

# Reports
Framework has been integrated with Allure-Reports
Run the following command to generate an HTML Report

```npx allure generate allure-results --clean && npx allure open```


