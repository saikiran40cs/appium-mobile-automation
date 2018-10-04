# Changing Context while testing an app {#tips-with-code-snippets}

Most of the time when you are testing an app, you will find that there is a specific page in app which is a Webview and your normal code is not working. So in those situations we need to change the application context to "**WEBVIEW**" or "**NATIVE**" accordingly. Below is a code snippet will do the same and change the context to Webview.

```
public static void changeDriverContextToWeb(AppiumDriver driver) {
        Set<String> contextNames = driver.getContextHandles();
        for (String contextName : contextNames) {
            if (contextName.contains("WEBVIEW"))
                DriverFactory.driver.context(contextName);
        }
    }
```

A similar code can be used with Native as parameter to change the context to Native app.

```
public static void changeDriverContextToNative(AppiumDriver driver) {
    Set<String> contextNames = driver.getContextHandles();
    for (String contextName : contextNames) {
        if (contextName.contains("NATIVE"))
            DriverFactory.driver.context(contextName);
    }
}
```



