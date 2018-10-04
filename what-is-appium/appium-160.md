# What is new in Appium 1.6.0 {#what-is-new-in-appium-160}

What's new in Appium 1.6 ?

* #### **UiAutomator 2** {#uiautomator-2}

With release of appium 1.6.0 , appium has started using **UiAutomator 2**

Till now appium was primarily dependent on Google's UiAutomator framework as the primary way of automating native Android apps.

To use UiAutomator 2, you can specify

> **automationName: uiautomator2**

in your desired capabilities and try out the new driver.

Prerequisites: This module should support from Android 5.0 \(API Level 20\) and above

For more info, check out the wiki article here: [https://github.com/appium/appium-uiautomator2-server/wiki](https://github.com/appium/appium-uiautomator2-server/wiki)

* #### **XCUITest** {#xcuitest}

Appium has added support for Apple's new XCUITest framework. When you specify a **platformVersion** of **10** or higher in Capabilities Builder, Appium automatically uses the XCUITest automation backend.

If you want to run your iOS test on version 9.3, then you need to specify

> **automationName: XCUITest**

in your desired capabilities.

