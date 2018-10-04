# How to get locators via Appium Inspector {#how-to-get-locators-via-appium-inspector}

In the previous chapter we saw **UiAutomatorViewer** which comes bundled with Android SDK. Appium has built something like that which makes our work of finding locators very easy.

When you start the Appium app, you would notice the icons at the top \(image below\), I have highlighted the Apppium Inspector in red.

![](/assets/appium_UI.png)

So if you notice that the appium server is running and the log shows that it's connected to the emulator running locally.When you click on the circled icon \(Appium Inspector\), it will launch a new UI as shown below with the application UI state captured.![](/assets/Inspector.png)

The panel on the extreme right is clickable and you can click on the element you want to find details about. So if you see the panel with title "**Details**", there are bunch of attributes listed for the highlighted element.

![](/assets/details.png)

If you notice the attribute "**resource-id**", it's made of the package name "**com.flipkart.android**" and the value of id attribute.

This **package name** is present for all the elements and hence we can externalize it. So to construct an element identifier for automation, we are going to use it as shown below:

```
String app_package_name = "com.flipkart.android:id/";
By userId = By.id(app_package_name + "user_id");
```

So the code would look like:

```
driver.findElement(userId).sendKeys("someone@saikiranpro.com");
```

Also you can use other options like xpath, index etc. Below is the snapshot of all the options you have for identifying the element.

![](/assets/findby.png)

