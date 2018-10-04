# Understanding Desired Capabilities {#understanding-desired-capabilities}

Before we start writing further test code to automate and do other stuff, we need to understand why we are using Desired Capabilities.

Desired Capabilities are present in the below library and hence it needs to be imported.

```
org.openqa.selenium.remote.DesiredCapabilities
```

Desired Capabilities is a way of telling the Appium Server which kind of session we are interested in. So it's a hash of Key and Value to let us have more control on the server during automation. So some of the key info which we will be using are :

```
automationName    Which automation engine to use    Appium (default) or Selendroid
platformName      Which mobile OS platform to use    iOS, Android, or FirefoxOS
```

Similarly, we can specify _platformVersion_ which will be the version of OS running on the device, could be "8.3" or "5.1".

Below is one such table which contains the various Desired Capabilities which would be set at the server level and customized to either Android or iOS.

| Capability | Description | Values |
| :--- | :--- | :--- |
| automationName | Which automation engine to use | Appium \(default\) or Selendroid |
| platformName | Which mobile OS platform to use | iOS, Android, or FirefoxOS |
| platformVersion | Mobile OS version | e.g., 7.1, 4.4 |
| deviceName | The kind of mobile device or emulator to use | iPhone Simulator, iPad Simulator, iPhone Retina 4-inch, Android Emulator, Galaxy S4, etc… |
| app | The absolute local path or remote http URL to an .ipa or .apk file, or a .zip containing one of these. Appium will attempt to install this app binary on the appropriate device first. Note that this capability is not required for Android if you specify appPackage and appActivity capabilities \(see below\). Incompatible with browserName. | /abs/path/to/my.apk or [http://myapp.com/app.ipa](http://myapp.com/app.ipa) |
| browserName | Name of mobile web browser to automate. Should be an empty string if automating an app instead. | ‘Safari’ for iOS and ‘Chrome’, ‘Chromium’, or ‘Browser’ for Android |
| newCommandTimeout | How long \(in seconds\) Appium will wait for a new command from the client before assuming the client quit and ending the session | e.g. 60 |
| autoLaunch | Whether to have Appium install and launch the app automatically. Default true | true, false |
| language | \(Sim/Emu-only\) Language to set for the iOS Simulator | e.g. fr |
| locale | \(Sim/Emu-only\) Locale to set for the iOS Simulator | e.g. fr\_CA |
| udid | Unique device identifier of the connected physical device | e.g. 1ae203187fc012g |
| orientation | \(Sim/Emu-only\) start in a certain orientation | LANDSCAPE or PORTRAIT |
| autoWebview | Move directly into Webview context. Default false | true, false |



