# How to get locators via UiAutomatorViewer {#how-to-get-locators-via-uiautomatorviewer}

**UIAutomatorviewer** comes packaged with Android sdk and is present under “_tools_” folder. It’s a tool, which lets you inspect the UI of an application in order to find the layout hierarchy, and view the properties associated with the controls.

While designing your UI automation suite, this tool is very helpful as it exposes the Id and other attributes of an element, which is needed for writing scripts.

Once the android sdk path is set on the machine, open the terminal and type

```
uiautomatorviewer
```

and this would launch the UI inspection tool. Below is how the tool looks like when no app is monitored.

![](/assets/UIAutomatorblank.png)

Clicking on the devices icon from left takes a dump of UI XML snapshot of the screen opened in the device. So you will be presented with an intermediate screen like this:

![](/assets/UIAutomatortakingscreenshot.png)

Once it finishes loading, this is how the tool looks like; we have highlighted the logo of Flipkart and the respective attribute details of the logo.

The left side of the tool shows how the device looks like and the right side is divided in two parts:

* Upper half to show the UI XML snapshot and the nodes structure
* Lower half shows the details of the node selected with all the attributes.

![](/assets/UIAutomatorFlipkartLogo.png)

So if you carefully look below, you would see the resource-id, which roughly translates to id of the HTML. And then there are other details like what is the class name, package it belongs to, whether it is enabled, whether it is selected etc.

![](/assets/UIAutomatorNodeDetail.png)

Apart from this all the UI elements on the left can be clicked upon and the right side changes dynamically to show the details of the element selected.

This detail pretty much about the UIAutomatorviewer.

