# Installing Appium {#installing-appium}

Download the Appium installer from the below mentioned location. Once done extract it and install the app.

```
https://github.com/appium/appium/releases

```

You can select the Android icon from the top and click on Launch.

![](/assets/appium.png)

Once the Appium server is running you will see some logs in the app screen or alternately hit the below url to check the status.

```
http://localhost:4723/wd/hub/status

```

Appium can also be run via npm install. For this you would need node.js and npm version \(0.10 or greater\). In order to verify if the appium is installed correctly and it's dependencies run the command

```
appium-doctor

```

This command can be supplied with flag --android to verify all the dependencies are set up properly.

The appium clients are simple extension to the WebDriver client.

