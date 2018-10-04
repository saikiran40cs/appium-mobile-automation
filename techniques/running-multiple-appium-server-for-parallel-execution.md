# Running multiple Appium Server for parallel execution {#running-multiple-appium-server-for-parallel-execution}

In the journey of mobile automation it would eventually happen that you will have substantial scenarios automated. Also the desire to have faster feedback would push the need for running **test in parallel**.

So how do you run the test in parallel ? One of the approach I would suggest here is to have multiple appium server running. Steps to do it:

* Connect couple of android devices to the system
* Run the below command and note down the device id.
  > adb devices
* Run the below command and replace the **udid** with actual device udid and port with values from \(4723\)
  > appium -U udid -p port
* For second device update the **udid** and increment the port value by 10

Appium gives a way to do the same via code by giving AppiumServiceBuilder class. Below is a sample code which takes input param as **port** and udid. In Appium 1.5.3 release they have move the udid to **GeneralServerFlag** as **Robot\_Address**.

`def service = AppiumDriverLocalService.buildService(new AppiumServiceBuilder() .usingDriverExecutable(new File("/Applications/Appium.app/Contents/Resources/node/bin/node")) .withAppiumJS(new File("/Applications/Appium.app/Contents/Resources/node_modules/appium/bin/appium.js")) .withIPAddress("127.0.0.1") .usingPort(port as int) .withArgument(GeneralServerFlag.ROBOT_ADDRESS, udid as String) .withArgument(AndroidServerFlag.BOOTSTRAP_PORT_NUMBER, ((port as int) + 2) as String) .withArgument(SESSION_OVERRIDE) .withLogFile(new File("build/${device}.log")));`

So the above command helps you create the appium service which then you can start as

> service.start

The next work would be to create a mapping of tag and the devices on which you want to run the test. This could be done via a properties file.

