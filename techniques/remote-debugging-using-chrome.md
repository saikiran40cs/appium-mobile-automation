# How to debug hybrid android app via Chrome browser {#how-to-debug-hybrid-android-app-via-chrome-browser}

In the previous chapter we saw **UIAutomatorviewer** and how to use that tool to look for elements and locators.

However, when you are working on a hybrid application \(developed on a platform like [Phonegap](http://phonegap.com/) \), we can use remote debugging.

To use Remote debugging, we need to have:

* Chrome \(version 69\) or later installed on your machine
* Android Device
  * Should be running Android 4.4+
  * USB Debugging enabled
* USB cable

Once the basic things are in place, connect your device to machine using USB cable. Launch Chrome and open a tab with target "_chrome://inspect_". This is how it would look like.

![](/assets/Screen Shot 2018-10-05 at 4.32.49 pm.png)

If you notice your phone, you would have got an alert saying "Allow USB Debugging".

![](/assets/USB_Debugging.png)

Once you click OK, your device would get showed up in browser tab. Below is how it would show up:

![](/assets/chrome-inspect-devices.png)

Once you click on **inspect**, you can see the locators as you have always done in web for Selenium.

![](/assets/remote-debug-banner.png)

You can also use Screen casting option by clicking the **Screencast** icon in the upper right corner of your remote debugging DevTools window.![](/assets/screencast-icon-location.png)

#### _This method of finding locator is faster than using UIAutomatorviewer and would be highly recommended._ {#this-method-of-finding-locator-is-faster-than-using-uiautomatorviewer-and-would-be-highly-recommended}



