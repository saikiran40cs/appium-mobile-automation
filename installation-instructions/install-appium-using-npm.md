# Install Appium using npm {#install-appium-via-source}

One of the alternative way to install Appium is to install via npm \(Node JS Package Manager\).

But before that you need to have below items installed

* npm \(version .10 or greater\)
* node.js

_Brew_ will be very handy here to install the above stuff. It's an amazing package manager for OS X and installing packages and updating it will be breeze once you install brew.

Once the node.js and npm are installed, you can use the below command to check if all the appium dependencies are met, run the below command:

```
appium-doctor
```

It would show up a result like this if everything is okay:

![](/assets/Appium-doctor.png)

Once done run the below command to install the appium:

```
npm install -g appium
```

Once this is done, start the appium server by the following command:

```
appium 
&
```



