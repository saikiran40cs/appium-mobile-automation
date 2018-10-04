# How to execute test on real android devices {#how-to-execute-test-on-real-android-devices}

This chapter would help you understand how to execute the test on real Android Devices, after all the biggest advantage of Appium is that you can run the same test on local devices.

For test to run on devices, we need to make sure :

* **USB Debugging** is enabled
* **ADB** lists your devices into the connected devices
* Changing the **Desired capability **as per the hardware

#### Enabling USB Debugging: {#enabling-usb-debugging}

By default, Android devices do not have USB Debugging enabled, these are under Developer Options. To turn them on,

* Navigate to Settings app on phone
* Scroll down and click on the Developer Options
* Turn on the Developer Options and click the USB Debugging.

![](/assets/DevOptions.png "Screen")

On the pop up \(shown below\), click on Ok.

![](/assets/USBDebug.png "Screen")

Some devices do not have “_Developer Options_” and hence the way to enable Debugging mode is to launch the Settings screen. Once done, tap “_About Phone_" and then scroll to the bottom and tap on "_Build Number_" 7 times \(Yes 7 times\)!

Once done, you will now be able to enable/disable it whenever you desire by going to

```
Settings -> Developer Options -> Debugging -> USB debugging
```

Once the above set ups are done, launch _Terminal_ \(or Command Prompt\) and type in

```
adb devices
```

On a happy path, it would show the below result.

![](/assets/adboutput.png)

There are times when even after starting USB mode on your device, adb wouldn’t list the device here. To fix that, below are some of the steps you need to follow:

* Open the USB manager on your laptop.
  * Use the vendor id \(highlighted in blue below\) and update in the **adb\_usb.ini** file.
  * Steps for MAC OS X to open the USB Manager:
    * Click on the Apple icon on top left of the screen
    * Click on “_About This Mac_”
    * On the pop up, click on the System Report
    * Under Hardware section, click on USB
    * You would notice the device connected there, click on the device.

![](/assets/USBMgr.png "Screen")

Once you have copied the **vendor ID**, we need to update the file below using the following command:

```
vim ~/.android/adb_usb.ini
```

This is how a sample file would look like after updating the Vendor ID.

![](/assets/androidIni.png "Screen")

Once the above changes are done, run the following commands:

```
adb kill-server
adb start-server
adb devices
```

This would finally show up the devices as connected. Once the device shows up as online, we are good to run the test.

Start the **Appium** and in that launch the **Android Server**.

In case you have any android version mentioned in your code, you can remove it and have only the one, which are mandatory. Below is a sample snippet I have used and works flawlessly.

```
File appDir = new File(“/Users/saikiranpro/Development/SampleApps”);
File app = new File(appDir, “Flipkart.apk”);
DesiredCapabilities capabilities = new DesiredCapabilities();
capabilities.setCapability(“device”,”Android”);
//mandatory capabilities
capabilities.setCapability(“deviceName”,”Android”);
capabilities.setCapability(“platformName”,”Android”);
capabilities.setCapability("udid", Properties.udid);

//other caps
capabilities.setCapability(“app”, app.getAbsolutePath());
driver = new RemoteWebDriver(new URL(“http://127.0.0.1:4723/wd/hub”), capabilities);
```

Whenever appium starts the appium.settings and unlock apps are installed in the device. For any test appium settings and unlock are the first apps appium server will interact then it will open the desired app as required

