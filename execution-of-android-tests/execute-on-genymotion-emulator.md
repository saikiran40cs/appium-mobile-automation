# How to run appium test on GenyMotion Emulator {#how-to-run-appium-test-on-genymotion-emulator}

## Introduction {#introduction}

A **Genymotion emulator** is a virtual device which runs on your system and like a typical android emulator. It's an emulator based on **Virtualbox**. It can emulate a bunch of android devices and support a wide variety of API levels. Since the Virtualbox is cross platform compatible, it allows Genymotion to be used on any platform be it windows, Linux, Mac. Genymotion allows you to create custom device image as well as standard device image which is easy to download and get started. It’s an emulator using x86 architecture virtualization, making it much more efficient.

Some of the features of Genymotion which stands out are:

* **Networking**: emulates WiFi connection
* **GPS**: allows coordinate configuration
* **Battery**: allows configuring battery levels
* **Display**: full screen display
* **Genymotion shell** which allows you to interact with your VM using a command line.
* **Performance**: very fast compared to android emulator

Genymotion has a free version and license one as well. Even in free version you will see a wide range of devices supported and the android version. Download and install the Genymotion app. Once done you should be able to log in with your registered credentials and launch the Genymotion app. This will open up a window shown below and give you option to choose device or android version.

**List of Device Image available**![](/assets/Screen Shot 2016-03-13 at 12.07.42 AM.png)

**List of Android Version supported**![](/assets/Screen Shot 2016-03-13 at 12.08.00 AM.png)

Once you download the required device image, if the app depends on Google Play, you need to do 2 things:

* install one apk "**com.android.vending-x.x.xx.apk**"
* Flash it with "**gapps-lp-YYYYMMDD-signed"**

## Running appium test on Genymotion emulator {#running-appium-test-on-genymotion-emulator}

To execute test on Genymotion emulator, you need to pass the emulator udid to the device config file. When you run "adb devices" command it will show you the udid of the running emulator. It would be typically like "192.168.57.101:5555". You need to pass this value against the udid in the device config file. This is not mandatory if you are running just one instance of emulator and appium server. But if you are attempting parallel run it will make sense to specify udid and bind it with one of the appium server.

