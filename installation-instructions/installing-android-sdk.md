# Installing Android {#installing-android}

## Android Requirements {#android-requirements}

* Android SDK API 
  &gt;
  = 17 \(Additional features require 18/19\)
* Appium supports Android on OS X, Linux and Windows.

**Android SDK** needs to be downloaded from the following location.

```
http://developer.android.com/sdk/index.html

```

Once you download the file and unzip, you would see the below structure in the sdk folder.

![](/assets/sdkFolder.png)

Post unzipping, update the system variable to include sdk as well. For mac users below are the command snapshot \(change the path and folder name accordingly as per your machine\)

```
export ANDROID_HOME=/Users/saikiran/Development/SDK
export PATH =${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools

```

Once this is done, we need to launch the SDK manager to download relevant files to create an emulator and run the virtual device. In terminal, type in

```
android sdk

```

This would open the SDK manager for you to download the relevant files. In the SDK manager select the below files as shown below. This will help you create a virtual device running Android 4.4.2.

![](/assets/androidsdkmgr.png)

Select the above files and choose to install, once done close the SDK manager. In terminal then type

```
android avd

```

This would open the Android Virtual Device Manager, which would help you create the virtual devices. Click on **Create** on the pop up opened and follow the below snapshot for the values. Select the **RAM** size as per your machine configuration.

![](/assets/avdmgr.png)

Once you have selected the above options, click on OK. Once done, it will show up in the AVD manager as below.

![](/assets/avdlist.png)

Select the AVD name and click on Start on the right. This would launch the pop up with few options, you may choose as you want.

![](/assets/launchoptions.png)

"_Wipe user data_" would wipe any previous app installation you have done and would launch a plain vanilla emulator.

Once done click on Launch, this will launch the emulator.

You can use the command “_adb devices”_ to see if the adb is detecting the emulator. This basically completes the android SDK installation part.

