# How to start appium server via Java code {#how-to-start-appium-server-via-java-code}

Appium has recently made some changes and now you can actually write a couple line of code and start appium server.

Appium has introduced a class called **AppiumDriverLocalService** which will help you do this. There are two ways you can write code:

1. If you have appium installed via npm then try the below lines of code.

   ```
    service = AppiumDriverLocalService.buildDefaultService();
    service.start();

   ```

    For stopping the appium server use:

   ```
    service.stop();

   ```

2. If you don't have appium installed via npm then try the below lines of code. For your local machine you might want to change the path accordingly. In the below example, I am showing if the OS is mac then use the installed Appium to start the server. If the OS is windows use the npm installed appium. This is just for the demonstration, ideally you should have common strategy whether it is Mac or Windows.

    String osName = System.getProperty\("os.name"\);

   ```
    if (osName.contains("Mac")) {
        service = AppiumDriverLocalService.buildService(new AppiumServiceBuilder()
                .usingDriverExecutable(new File("/Applications/Appium.app/Contents/Resources/node/bin/node"))
                .withAppiumJS(new File("/Applications/Appium.app/Contents/Resources/node_modules/appium/bin/appium.js"))
                .withIPAddress("127.0.0.1")
                .usingPort(port)
                .withLogFile(new File("target/"+deviceUnderExecution+".log")));
    } 
    else if (osName.contains("Windows")) {
        service = AppiumDriverLocalService.buildService(new AppiumServiceBuilder()
                .usingPort(port)
                .withLogFile(new File("target/"+deviceUnderExecution+".log")));
    } 
    else {
        Assert.fail("Unspecified OS found, Appium can't run");
    }

    System.out.println("- - - - - - - - Starting Appium Server- - - - - - - - ");
    service.start();

   ```

In the code above, I have the port as parameter for parallel runs on device.

However for windows you can use npm or the appium desktop so as to launch the server.

