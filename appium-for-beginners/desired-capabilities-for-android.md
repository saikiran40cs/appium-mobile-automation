# Desired Capabilities for Android {#desired-capabilities-for-android}

Since **Appium** caters to both Android and iOS, there are different set of desired capabilities for Android and iOS.

This section will list all the desired capabilities associated with Android. Majority of them are optional but you can choose to use them as it suits your needs.

| Capability | Description | Values |
| :--- | :--- | :--- |
| appActivity | Activity name for the Android activity  you want to launch from your package | MainActivity, .Settings |
| appPackage | Java package of the Android app you want to run | com.example.android.myApp, com.android.settings |
| appWaitActivity | Activity name for the Android activity  you want to wait for | SplashActivity |
| appWaitPackage | Java package of the Android app you want to wait for | com.example.android.myApp, com.android.settings |
| deviceReadyTimeout | Timeout in seconds while waiting for  device to become ready | 5 |
| androidCoverage | Fully qualified instrumentation class.  Passed to -w in adb shell am instrument -e coverage true -w | com.my.Pkg/com.my.Pkg.instrumentation.MyInstrumentation |
| enablePerformanceLogging | \(Chrome and webview only\) Enable Chromedriver’s performance logging \(default false\) | true, false |
| androidDeviceReadyTimeout | Timeout in seconds used to wait for a device to become ready after booting | e.g., 30 |
| androidDeviceSocket | Devtools socket name. Needed only when tested app is a Chromium embedding browser. The socket is open by the browser and Chromedriver connects to it as a devtools client. | e.g., chrome\_devtools\_remote |
| avd | Name of avd to launch | e.g., api19 |
| avdLaunchTimeout | How long to wait in milliseconds for an avd to launch and connect to ADB \(default 120000\) | 300000 |
| avdReadyTimeout | How long to wait in milliseconds for an avd to finish its boot animations \(default 120000\) | 300000 |
| avdArgs | Additional emulator arguments used when launching an avd | e.g., -netfast |
| useKeystore | Use a custom keystore to sign apks, default false | true or false |
| keystorePath | Path to custom keystore, default ~/.android/debug.keystore | e.g., /path/to.keystore |
| keystorePassword | Password for custom keystore | e.g., foo |
| keyAlias | Alias for key | e.g., androiddebugkey |
| keyPassword | Password for key | e.g., foo |
| chromedriverExecutable | The absolute local path to webdriver executable \(if Chromium embedder provides its own webdriver, it should be used instead of original chromedriver bundled with Appium\) | /abs/path/to/webdriver |
| specialChromedriverSessionArgs | Custom arguments passed directly to chromedriver in chromeOptions capability. Passed as object which properties depend on a specific webdriver. | e.g., {'androidDeviceSocket': 'opera\_beta\_devtools\_remote',} |
| autoWebviewTimeout | Amount of time to wait for Webview context to become active, in ms. Defaults to 2000 | e.g. 4 |
| intentAction | Intent action which will be used to start activity \(default android.intent.action.MAIN\) | e.g.android.intent.action.MAIN, android.intent.action.VIEW |
| intentCategory | Intent category which will be used to start activity \(default android.intent.category.LAUNCHER\) | e.g. android.intent.category.LAUNCHER, android.intent.category.APP\_CONTACTS |
| intentFlags | Flags that will be used to start activity \(default 0x10200000\) | e.g. 0x10200000 |
| optionalIntentArguments | Additional intent arguments that will be used to start activity. See Intent arguments | e.g. --esn, --ez, etc. |
| unicodeKeyboard | Enable Unicode input, default false | true or false |
| resetKeyboard | Reset keyboard to its original state, after running Unicode tests with unicodeKeyboard capability. Ignored if used alone. Default false | true or false |

If you notice above some of the capabilities like _appWaitActivity_ , _avd_, _androidDeviceReadyTimeout_ are very handy and would be recommended to make use of in your automation suite.

